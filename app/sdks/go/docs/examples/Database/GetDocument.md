# Database Examples

## GetDocument

```go
    package appwrite-getdocument

    import (
        "fmt"
        "os"
        "github.com/appwrite/sdk-for-go"
    )

    func main() {
        // Create a Client
        var clt := appwrite.Client{}

        // Set Client required headers
        clt.SetProject("")
        clt.SetKey("")

        // Create a new Database service passing Client
        var srv := appwrite.Database{
            client: &clt
        }

        // Call GetDocument method and handle results
        var res, err := srv.GetDocument("[COLLECTION_ID]", "[DOCUMENT_ID]")
        if err != nil {
            panic(err)
        }

        fmt.Println(res)
    }
```