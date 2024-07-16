# ollama-docker-macOS

## Run the project

### Docker

To run the docker image, please use the following command: `docker compose up --build`. To kill the program you can run: `docker compose down`

If everything is setup correctly, the first thing the program will do is to download the model you specified in the `.env` file in the field `LLM = "llama3"`. This process can take quiet some time so you will need to be patient.

In case you wish to use a different LLM than LLAMA3, please look [here](https://ollama.com/library) for a detailed list of all the models compatible with `Ollama`. 

### Curl 

To run the LLM locally you can run the following command: 

```shell
curl -X POST http://localhost:11434/api/generate \
     -H "Content-Type: application/json" \
     -d '{"model": "llama3", "prompt": "tell me a joke"}'
```

The response should be something along these lines: 

```shell
{"model":"llama3","created_at":"2024-07-16T08:22:29.059892387Z","response":"Here","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:29.203693804Z","response":"'s","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:29.332379846Z","response":" one","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:29.470641804Z","response":":\n\n","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:29.607131262Z","response":"Why","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:29.726561721Z","response":" couldn","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:29.866282721Z","response":"'t","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:30.071196388Z","response":" the","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:30.236524429Z","response":" bicycle","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:30.352074013Z","response":" stand","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:30.463630638Z","response":" up","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:30.581548721Z","response":" by","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:30.693218971Z","response":" itself","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:30.815420055Z","response":"?\n\n","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:30.93863793Z","response":"(wait","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:31.058018263Z","response":" for","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:31.173991638Z","response":" it","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:31.284384846Z","response":"...)\n\n","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:31.40713068Z","response":"Because","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:31.52646343Z","response":" it","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:31.64686843Z","response":" was","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:31.863791138Z","response":" two","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:31.983446347Z","response":"-t","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:32.451686847Z","response":"ired","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:32.650440097Z","response":"!\n\n","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:32.784451083Z","response":"Hope","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:32.89752975Z","response":" that","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:33.018939541Z","response":" made","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:33.132293166Z","response":" you","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:33.239832583Z","response":" smile","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:33.351897791Z","response":"!","done":false}
{"model":"llama3","created_at":"2024-07-16T08:22:33.496378667Z","response":"","done":true,"done_reason":"stop","context":[128006,882,128007,271,73457,757,264,22380,128009,128006,78191,128007,271,8586,596,832,1473,10445,7846,956,279,36086,2559,709,555,5196,1980,65192,369,433,62927,18433,433,574,1403,2442,2757,2268,39115,430,1903,499,15648,0],"total_duration":29484346972,"load_duration":24044057178,"prompt_eval_count":14,"prompt_eval_duration":1001881000,"eval_count":32,"eval_duration":4435942000}
```