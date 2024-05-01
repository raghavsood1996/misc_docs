
```mermaid
classDiagram
    class BaseJson {
        +toJson(): string
        +fromJson(json: string): void
    }

    class TaskPlanMetadata {
        +is_plan_partial: bool
        +start_trim: double
        +end_trim: double
        +planned_roll: vector<double>
        +planned_slope: vector<double>
        +fromRosMsg(TaskPlanMetaDataMsg) : TaskPlanMetadata
        +toRosMsg() : TaskPlanMetadataMsg
    }

    BaseJson <|-- TaskPlanMetadata
    ```