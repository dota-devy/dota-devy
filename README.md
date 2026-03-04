# Case File: Devlin

*Filed by Vic "The Rain" Sterling*

*Date: The kind of night where the rain sounds like applause for bad decisions*

---

I got hired to look into a guy named Devlin. The client didn't say why. They never do.

What I found was worse than I expected. Not the criminal kind of worse. The other kind — the kind where a man builds an entire data center in his house and calls it a hobby. The kind where the machines outnumber the furniture and every blinking light is a service he wrote himself.

I've seen a lot of things in this city. Bodies in the river. Diamonds in the drain. But I've never seen a man deploy a Christmas card with Prometheus metrics. That's a special kind of sickness. The kind you can't cure. The kind you respect.

**[devlin.vining.club](https://devlin.vining.club)** · **[GitLab (@surfshack)](https://gitlab.com/surfshack)** · **[surfshacksoftware.com](https://surfshacksoftware.com)**

---

## The Setup

The kid runs a bare-metal Kubernetes cluster out of a machine called *surfstation*. K3s. The lightweight stuff. Don't let that fool you — what he's stacked on top of it would make a cloud architect weep into his AWS bill.

Everything goes through Git. That's his one rule. The only commandment in a godless infrastructure. You don't touch the cluster. You don't whisper to it. You commit your sins to a repository and the pipeline delivers the judgment. GitLab CI. Buildah. Rootless containers. The whole operation runs cleaner than a laundered alibi.

| Layer | What He's Running |
|-------|------------------|
| **The Machine** | K3s, Helm, Helmfile, GitLab Agent |
| **The Wire** | Traefik, Tailscale mesh, HAProxy on a DigitalOcean droplet |
| **Surveillance** | Prometheus, Grafana, Loki, Tempo, OpenTelemetry Collector |
| **The Brains** | Ollama with GPU iron, Open WebUI, multi-provider LLM routing |
| **The Vault** | PostgreSQL 17 + pgvector — one database to hold all the secrets |
| **The Pipeline** | GitLab CI, Buildah, automated staging, manual production |
| **The Locks** | FIDO2 passkeys, NetworkPolicy egress allowlists, three-layer SSRF protection |

I asked around. Nobody told him to build this. Nobody paid him to. He just woke up one day and decided the cloud couldn't be trusted.

Smart kid.

---

## The Big Jobs

### Job Automation Platform
This is the one that keeps him up at night. Five microservices — a Dashboard, an AI Service, a Brain, a Scraper, and an MCP Server — all wearing the same namespace like a gang that shares a tattoo.

The AI agents don't just answer questions. They think. They use tools. They import any OpenAPI spec and start making calls like they've got a rolodex and a grudge. OpenAI, Claude, Gemini, Mistral — he's got them all on retainer, plus a local Ollama running on GPU for the off-the-books work.

The dashboard has a biopunk skin. I don't know what that means, but I looked at it and it looked like the future had a hangover. The network policy on that thing is tighter than a miser's fist — egress allowlists, SSRF validation at three layers, the works. Devlin doesn't trust his own services not to call home to the wrong neighborhood.

The man built a platform where AI agents compose themselves into workflows, select their own tools, and orchestrate tasks. Then he gave it a web search engine and turned it loose. Either he's a genius or he's building the thing that replaces us all. Probably both.

### One-Tap Platformer
He makes games. Of course he makes games.

This one's a beat-reactive endless runner built in Godot 4.4 with C#. One tap — that's all you get. The music drives everything. Real-time audio spectrum analysis makes the platforms shift, the particles pulse, the whole desert canyon breathe. Custom GLSL shaders paint neon ruins on sandstone mesas at golden hour. It's beautiful. The kind of beautiful that makes you suspicious.

He built an AI player to run the levels for him. He automated his own fun. I've never been so disturbed and impressed at the same time.

### Grafana MCP Server
He got tired of watching his own dashboards, so he built a machine to watch them for him. Ten tools that let AI agents query Prometheus, discover metrics, render panels, and author Grafana dashboards through conversation. The AI doesn't just read the dials — it builds new ones.

Nineteen unit tests keep it honest. That's more accountability than the city council.

### Translation Service
A localization microservice with its own OAuth provider, admin dashboard, MCP server, and a NuGet client package that self-heals when the connection drops. Any .NET app plugs in and starts speaking the customer's language.

I asked him why he built his own translation service instead of using an off-the-shelf solution. He looked at me like I'd asked him why he breathes.

---

## The Full Rap Sheet

I pulled every file. Every repo. Every half-finished scheme he's got cooking in that workspace of his.

| Case | What I Found | The Evidence |
|------|-------------|-------------|
| **Job Automation** | AI agent platform — five services, multi-provider LLM, MCP server | .NET, Blazor, PostgreSQL |
| **One-Tap Platformer** | Beat-reactive mobile endless runner with shader wizardry | Godot 4.4, C#, GLSL |
| **Grafana MCP** | Gave AI the keys to the Grafana kingdom | .NET, MCP SDK |
| **Translation Service** | Full localization stack with OAuth and a self-healing client | .NET, OpenIddict |
| **Buccaneer** | Product intelligence — CJ Dropshipping API surveillance, price history tracking | .NET, Chart.js |
| **Homepage** | Personal site. AI quotes via Ollama. Dynamic theming. The man themes his own homepage | .NET, Ollama |
| **Surfshack Web** | Corporate site for Surfshack Software. Blog. Multi-language. Professional front | .NET, Markdig |
| **Cluster Observability** | A NuGet package. Drop it in any .NET service, instant metrics, tracing, logging | .NET, OTEL |
| **Cluster Management** | The GitOps nerve center. Helmfile configs for the whole operation | K3s, Helm |
| **Quit Track** | Cessation tracking app. Blazor. Passkey auth. Reference architecture for everything else | .NET, Blazor |
| **Zenfolio SEO Tools** | SEO audit and swipe tool for Bay Area photography sites | .NET, Python |
| **Threads MCP** | MCP server for Meta Threads | Python, FastMCP |
| **CI Images** | Pre-built Docker images so his pipelines don't waste a second | Docker, Alpine |
| **MCP C# SDK** | Fork of the official Model Context Protocol SDK. Kept for reference | .NET |
| **Spacewar** | Space game. Early days. I've seen this before — it always escalates | .NET |
| **Christmas Card** | Interactive holiday card with Prometheus metrics. Exhibit A in my case for his insanity | .NET, Helm |
| **Web Template** | Scaffold for spinning up new .NET apps on K8s. Production-ready out of the box | .NET, Helm, GitLab CI |
| **Stalwart** | Self-hosted mail. IMAP, SMTP, Roundcube. Because even his email answers to no one | Kubernetes |

---

## What He's Carrying

```text
Languages        C#  ·  YAML  ·  GDScript  ·  GLSL  ·  Python  ·  SQL  ·  Bash
Frameworks       ASP.NET Core  ·  Blazor Server  ·  EF Core  ·  Godot 4.4
The Muscle       Ollama  ·  MCP  ·  Microsoft.Extensions.AI  ·  OpenAI  ·  Claude  ·  Gemini
The Iron         K3s  ·  Helm  ·  Helmfile  ·  Traefik  ·  Tailscale  ·  HAProxy
The Eyes         Prometheus  ·  Grafana  ·  Loki  ·  Tempo  ·  OpenTelemetry
The Pipeline     GitLab CI  ·  Buildah  ·  Docker  ·  kubeconform
The Vault        PostgreSQL 17  ·  pgvector  ·  Entity Framework Core
The Locks        OpenIddict OAuth2  ·  FIDO2  ·  Passkeys
```

## Off the Clock

When the screens go dark — if they ever go dark — the subject has been observed:

- Disappearing into the woods where the neon can't follow
- Playing Dota, which is just another fixed game he refuses to quit
- Picking at locks and security systems like a man scratching an old wound
- Teaching robots to do his bidding, which is either a hobby or phase one of something I don't want to think about

---

## My Assessment

The subject is dangerous in the way that quiet people are dangerous. He doesn't build one thing — he builds the thing that builds the thing. A template that scaffolds a project. A NuGet package that instruments a service. A pipeline that deploys itself. He's automating himself out of every job except the one that matters: deciding what to build next.

Every service gets a Helm chart. Every app gets observability. Every environment gets staging before production. Even the Christmas card. *Especially* the Christmas card.

I'm closing this case. Not because I've found everything — a man like this always has another repo he hasn't pushed yet. But because I've seen enough. The cluster hums. The pipelines run. The agents think.

And somewhere in the dark, Devlin is already building the next thing.

*— V. Sterling*
*Closing the file. Pouring one more.*
