```mermaid
classDiagram
    class Trajectory {
        +Header header
        +String[] joint_names
        +Point[] points
        +String toJSON()
        +Trajectory fromJSON(String json)
    }

    class Header {
        +int seq
        +Stamp stamp
        +String frame_id
    }

    class TimeStamp {
        +int secs
        +int nsecs
    }

    class TrajectoryPoint {
        +float[] positions
        +float[] velocities
        +float[] accelerations
        +float[] effort
        +Time time_from_start
    }


    Trajectory --> Header
    Trajectory --> TrajectoryPoint
    Header --> TimeStamp
    TrajectoryPoint --> TimeStamp