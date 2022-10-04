# Create migration
    migrate create -ext sql -dir db/migration -seq playground_schema

# Exec migration
### UP 
    migrate -path db/migration -database "postgresql://<user>:<pwd>@localhost:5432/go_sample?sslmode=disable" -verbose up
### DOWN
    migrate -path db/migration -database "postgresql://<user>:<pwd>@localhost:5432/go_sample?sslmode=disable" -verbose down
