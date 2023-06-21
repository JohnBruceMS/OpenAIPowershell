# OpenAIPowershell
Super simple function to call chatgpt from your own code.  Insert your API key and go.

## SYNOPSIS
    Invokes the OpenAI API to generate a response to a given prompt.

## PARAMETER ApiKey
    The OpenAI API key to use for authentication.

## PARAMETER Model
    The OpenAI model to use for generating the response.
## PARAMETER Prompt
    The prompt to use for generating the response.
## EXAMPLE
    $apiKey = "<Your-Key>"
    $model = "gpt-3.5-turbo-16k"
    $prompt = "You are a helpful assistant. Tell me something interesting you can help me with?"
    $result = Invoke-OpenAI -ApiKey $apiKey -Model $model -Prompt $prompt
    Write-Host "Response from OpenAI API: $result"

## NOTES
    This function requires an OpenAI API key to work. You can get one by signing up for an OpenAI account 
    at https://platform.openai.com/account/api-keys Your API key is a secret that should not be shared
    with others or exposed in any client-side code. Store it in a secure location and use environment 
    variables or a secret management service to access it in your code.

Sample Model types OpenAI models:
-   gpt-4:         A set of models that improve on GPT-3.5 and can understand as well as generate natural language 
                or code. Use this model for complex tasks that require advanced reasoning and general knowledge1.
-   gpt-3.5-turbo: A set of models that improve on GPT-3 and can understand as well as generate natural language or 
                code. Use this model for chat applications or traditional completion tasks1.
-  gpt-3.5-turbo-16k: A model that offers 4 times the context length of gpt-3.5-turbo at twice the price. Use this 
                model for longer chat sessions or documents2.
-  code-davinci: A model that can understand and generate code, including translating natural language to code. Use 
                this model for coding tasks or queries3.

This script requires the Microsoft.PowerShell.Utility module to be imported for the ConvertTo-Json cmdlet. 

