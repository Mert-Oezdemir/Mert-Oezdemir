# Awesome Computer-Use Agents & Automation

[English](#english) · [Türkçe](#türkçe)

A bilingual, curated guide to 17 public GitHub repositories for computer-use agents, browser automation, remote access, isolated multi-agent environments and game-playing AI.

Bilgisayar kullanan agent'lar, tarayıcı otomasyonu, uzaktan erişim, izole çoklu agent ortamları ve oyun oynayan yapay zekâ için 17 herkese açık GitHub reposundan oluşan iki dilli rehber.

> Repository accessibility and archive status checked on 2026-11-25. This is an independent directory, not a benchmark, security audit, endorsement, or claim that all projects are fully open source or self-hostable.
>
> Depoların erişilebilirliği ve arşiv durumu 25.11.2026 tarihinde kontrol edilmiştir. Bu bağımsız bir rehberdir; performans testi, güvenlik denetimi, resmî onay veya tüm projelerin tamamen açık kaynak ve bağımsız çalışabilir olduğuna dair bir iddia değildir.

## English

### Repository directory

| # | Repository | Focus | Best suited for | Important limitations |
| --- | --- | --- | --- | --- |
| 1 | [Cua](https://github.com/trycua/cua) | Desktop / isolation | Computer-use infrastructure, virtual desktops, VM and sandbox tooling for isolated agent workloads. | Platform support and isolation depend on the selected component; review each component. |
| 2 | [Agent S](https://github.com/simular-ai/Agent-S) | Desktop agent / reasoning | Research framework for GUI grounding, task planning, reasoning and computer interaction. | Requires a compatible model and execution environment; not a guaranteed autonomous operator. |
| 3 | [Playwright](https://github.com/microsoft/playwright) | Browser automation | Programmatic control of Chromium, Firefox and WebKit, browser contexts, testing and tracing. | Automation engine, not an autonomous decision-maker. |
| 4 | [Agent Browser](https://github.com/vercel-labs/agent-browser) | Agent browser tooling | Browser interaction tools for AI agents, page snapshots, clicking, typing and session management. | Browser automation is not equivalent to full desktop isolation. |
| 5 | [Steel Browser](https://github.com/steel-dev/steel-browser) | Browser infrastructure | Self-hostable browser infrastructure with session APIs and automation integrations. | Configure network boundaries, authentication and resource limits. |
| 6 | [OpenAdapt](https://github.com/OpenAdaptAI/OpenAdapt) | Desktop workflows | Recording, learning and replaying desktop workflows; useful for repetitive tasks and demonstrations. | Compatibility and replay reliability depend on the environment. |
| 7 | [Browser Use](https://github.com/browser-use/browser-use) | Autonomous web agent | Model-driven web navigation, form filling, research and multi-step browser tasks. | Local execution is possible; model and optional hosted services may introduce external dependencies. |
| 8 | [Skyvern](https://github.com/Skyvern-AI/skyvern) | Web workflows | AI-assisted automation of complex forms, portals, data extraction and multi-step workflows. | Check self-hosted feature coverage and licensing obligations. |
| 9 | [Desktop Commander MCP](https://github.com/wonderwhy-er/DesktopCommanderMCP) | Local system tools | MCP tools for terminal sessions, files, search and code editing on a computer. | High-privilege capability; use least privilege and a real isolation boundary. |
| 10 | [ULPI Browse](https://github.com/ulpi-io/browse) | Parallel browser sessions | Browser infrastructure aimed at parallel, isolated browser sessions for agents. | Evaluate isolation strength and production maturity before adoption. |
| 11 | [TinyFish MCP Server](https://github.com/tinyfish-io/tinyfish-mcp-server) | Hosted service connector | Local MCP proxy to the hosted TinyFish web automation service. | Not the full automation backend; the default setup requires a hosted endpoint and API key. |
| 12 | [Remote Desktop Commander](https://github.com/desktop-commander/remote-desktop-commander) | Remote access integration | Documentation and manifests for remote computer access via MCP. | The hosted relay/backend is not fully included in this repository; not a complete self-hosted replacement. |
| 13 | [Voyager](https://github.com/MineDojo/Voyager) | Minecraft agents | Research agent for Minecraft exploration, skill acquisition and open-ended tasks. | Game-specific environment and model dependencies; not a general-purpose game player. |
| 14 | [Pokémon Agent](https://github.com/NousResearch/pokemon-agent) | Pokémon agents | Research tooling for AI agents playing Pokémon and tracking game state. | Game/emulator compatibility and model setup matter. |
| 15 | [Gamer](https://github.com/RainBowLuoCS/Gamer) | Real-time 3D game research | Vision-language-action research for real-time 3D game interaction. | Experimental; hardware, game support and latency are important constraints. |
| 16 | [GameCLI-Agent](https://github.com/BjornBrorsson/GameCLI-Agent) | Turn-based game agents | Screen-driven game interaction using mouse and keyboard, particularly suited to slower-paced games. | Not a universal real-time game controller. |
| 17 | [Bytebot](https://github.com/bytebot-ai/bytebot) | Containerized desktop | Container-based Linux desktop agent for GUI and application workflows. | Archived upstream; reference only, not recommended as a new production dependency. |

### Suggested architecture

A practical starting point is to combine **Cua** for isolated execution, **Agent S** for GUI reasoning, **Playwright** for deterministic browser automation, and **Agent Browser** or **Steel Browser** where session tooling or browser infrastructure is needed. Add **Desktop Commander MCP** for controlled file/terminal operations and **OpenAdapt** for repetitive GUI tasks if appropriate. Browser Use and Skyvern are alternatives for higher-level web tasks; game-specific agents should be evaluated separately.

For multiple agents, isolate desktops/browser sessions, user profiles, credentials and resources. Use a task scheduler, locks for shared files, restricted network access, audit logs, and approval gates for sensitive actions. Browser contexts alone are not necessarily a security boundary. These components are not an integrated, tested product; adapters and compatibility testing are required.

### Security, privacy and licensing

- Inspect source, dependencies, installation scripts, binary provenance and network traffic before granting desktop or filesystem access.
- Use isolated VMs or appropriately hardened sandboxes and non-administrator accounts. Avoid exposing personal browser profiles, passwords, tokens or SSH keys to agents.
- Prefer pinned, reviewed versions. Monitor upstream security fixes and verify software artifacts; merely cloning a repository does not make it secure.
- TinyFish MCP Server and Remote Desktop Commander rely on hosted components in their documented default architecture. A Git clone does not provide their full hosted backend.
- Bytebot is archived; treat it as a historical reference. Research systems may be experimental and game automation must respect applicable game rules.
- Check each upstream project's license and dependency licenses before redistributing or incorporating code. This guide links to upstream repositories; it does not relicense or mirror their source code.

## Türkçe

### Repo rehberi

| # | Repo | Odak alanı | En uygun olduğu işler | Önemli sınırlamalar |
| --- | --- | --- | --- | --- |
| 1 | [Cua](https://github.com/trycua/cua) | Masaüstü / izolasyon | Bilgisayar kontrolü, sanal masaüstleri, VM ve sandbox araçlarıyla agent görevlerinin izolasyonu. | Platform desteği ve izolasyon seçilen bileşene bağlıdır; bileşenleri ayrı inceleyin. |
| 2 | [Agent S](https://github.com/simular-ai/Agent-S) | Masaüstü agent'ı / karar | Grafik arayüzü algılama, görev planlama, karar verme ve bilgisayarla etkileşim için araştırma çatısı. | Uyumlu model ve çalışma ortamı gerektirir; kusursuz otonomi garantisi yoktur. |
| 3 | [Playwright](https://github.com/microsoft/playwright) | Tarayıcı otomasyonu | Chromium, Firefox ve WebKit kontrolü, tarayıcı oturumları, test ve işlem izleme. | Otomasyon motorudur; tek başına otonom karar vermez. |
| 4 | [Agent Browser](https://github.com/vercel-labs/agent-browser) | Agent tarayıcı araçları | AI agent'lar için sayfa anlık görüntüleri, tıklama, yazma ve oturum yönetimi. | Tarayıcı otomasyonu tam masaüstü izolasyonu değildir. |
| 5 | [Steel Browser](https://github.com/steel-dev/steel-browser) | Tarayıcı altyapısı | Kendi altyapınızda barındırılabilen tarayıcı oturum API'leri ve otomasyon entegrasyonları. | Ağ sınırları, kimlik doğrulama ve kaynak limitleri yapılandırılmalıdır. |
| 6 | [OpenAdapt](https://github.com/OpenAdaptAI/OpenAdapt) | Masaüstü iş akışları | Masaüstü iş akışlarını kaydetme, öğrenme ve tekrarlama; rutin görevler ve demonstrasyonlar. | Uyumluluk ve tekrar güvenilirliği çalışma ortamına bağlıdır. |
| 7 | [Browser Use](https://github.com/browser-use/browser-use) | Otonom web agent'ı | Model destekli web gezinme, form doldurma, araştırma ve çok adımlı tarayıcı görevleri. | Yerel çalışma mümkündür; model ve isteğe bağlı bulut hizmetleri dış bağımlılık oluşturabilir. |
| 8 | [Skyvern](https://github.com/Skyvern-AI/skyvern) | Web iş akışları | Karmaşık formlar, portallar, veri çıkarma ve çok adımlı web iş akışlarının AI destekli otomasyonu. | Self-hosted sürümün özellik kapsamı ve lisans yükümlülükleri kontrol edilmelidir. |
| 9 | [Desktop Commander MCP](https://github.com/wonderwhy-er/DesktopCommanderMCP) | Yerel sistem araçları | Bilgisayarda terminal oturumları, dosyalar, arama ve kod düzenleme için MCP araçları. | Yüksek yetkili araçlardır; asgari yetki ve gerçek izolasyon kullanın. |
| 10 | [ULPI Browse](https://github.com/ulpi-io/browse) | Paralel tarayıcı oturumları | Agent'lar için paralel ve birbirinden ayrılmış tarayıcı oturumları hedefleyen altyapı. | Kullanmadan önce izolasyon gücü ve üretim olgunluğu değerlendirilmelidir. |
| 11 | [TinyFish MCP Server](https://github.com/tinyfish-io/tinyfish-mcp-server) | Bulut hizmeti bağlantısı | TinyFish'in barındırılan web otomasyon hizmetine bağlanan yerel MCP proxy. | Tam otomasyon sunucusu değildir; varsayılan kurulum uzak uç nokta ve API anahtarı gerektirir. |
| 12 | [Remote Desktop Commander](https://github.com/desktop-commander/remote-desktop-commander) | Uzaktan erişim entegrasyonu | MCP üzerinden uzaktan bilgisayar erişimi için belgeler ve entegrasyon manifestleri. | Barındırılan relay/backend bu repoda bütünüyle bulunmaz; tam bağımsız bir alternatif değildir. |
| 13 | [Voyager](https://github.com/MineDojo/Voyager) | Minecraft agent'ları | Minecraft'ta keşif, beceri edinme ve açık uçlu görevler için araştırma agent'ı. | Oyuna özgü ortam ve model bağımlılıkları vardır; genel amaçlı oyun oyuncusu değildir. |
| 14 | [Pokémon Agent](https://github.com/NousResearch/pokemon-agent) | Pokémon agent'ları | Pokémon oynayan ve oyun durumunu izleyen AI agent'ları için araştırma araçları. | Oyun/emülatör uyumluluğu ve model kurulumu önemlidir. |
| 15 | [Gamer](https://github.com/RainBowLuoCS/Gamer) | Gerçek zamanlı 3D oyun araştırması | Gerçek zamanlı 3D oyun etkileşimi için görüntü-dil-eylem araştırması. | Deneyseldir; donanım, oyun desteği ve gecikme önemli sınırlardır. |
| 16 | [GameCLI-Agent](https://github.com/BjornBrorsson/GameCLI-Agent) | Sıra tabanlı oyun agent'ları | Ekran görüntüsü, fare ve klavye ile oyun etkileşimi; özellikle yavaş tempolu oyunlar için uygundur. | Evrensel gerçek zamanlı oyun kontrolcüsü değildir. |
| 17 | [Bytebot](https://github.com/bytebot-ai/bytebot) | Container masaüstü | Grafik arayüz ve uygulama iş akışları için container tabanlı Linux masaüstü agent'ı. | Kaynak depo arşivlenmiştir; referans olarak inceleyin, yeni üretim bağımlılığı olarak önermiyoruz. |

### Önerilen mimari

İzole çalışma ortamı için **Cua**, grafik arayüzü anlama ve karar verme için **Agent S**, deterministik tarayıcı otomasyonu için **Playwright**; gerektiğinde oturum yönetimi veya tarayıcı altyapısı için **Agent Browser** ya da **Steel Browser** iyi bir başlangıç olabilir. Kontrollü dosya/terminal erişimi için **Desktop Commander MCP**, tekrarlayan grafik arayüz görevleri için **OpenAdapt** eklenebilir. Browser Use ve Skyvern daha üst düzey web görevleri için alternatiflerdir. Oyuna özgü agent'lar ayrı değerlendirilmelidir.

Birden fazla agent çalıştırırken masaüstü/tarayıcı oturumları, kullanıcı profilleri, kimlik bilgileri ve kaynaklar birbirinden ayrılmalıdır. Görev zamanlayıcısı, ortak dosya kilitleri, sınırlı ağ erişimi, denetim kayıtları ve hassas işlemler için onay mekanizması kullanılmalıdır. Tarayıcı context'leri tek başına güvenlik sınırı sayılmayabilir. Bu bileşenler hazır ve birlikte test edilmiş bir ürün değildir; entegrasyon ve uyumluluk testleri gerektirir.

### Güvenlik, gizlilik ve lisanslar

- Masaüstü veya dosya sistemi yetkisi vermeden önce kaynak kodu, bağımlılıkları, kurulum betiklerini, ikili dosyaların kökenini ve ağ trafiğini inceleyin.
- İzole sanal makineler veya uygun şekilde güçlendirilmiş sandbox ortamları ve yönetici yetkisi olmayan hesaplar kullanın. Kişisel tarayıcı profillerini, parolaları, erişim anahtarlarını ve SSH anahtarlarını agent'lara açmayın.
- İncelenmiş, sabitlenmiş sürümleri tercih edin; güvenlik güncellemelerini takip edin ve yazılım dosyalarını doğrulayın. Bir repoyu kopyalamak onu güvenli yapmaz.
- TinyFish MCP Server ve Remote Desktop Commander belgelenen varsayılan mimarilerinde barındırılan hizmetlere bağlıdır. Git kopyası, bulut tarafındaki altyapının tamamını sağlamaz.
- Bytebot arşivlenmiş bir projedir; tarihsel referans olarak değerlendirin. Araştırma projeleri deneysel olabilir ve oyun otomasyonu ilgili oyun kurallarına uygun olmalıdır.
- Kaynak kodu yeniden dağıtmadan veya projenize entegre etmeden önce her kaynak deponun ve bağımlılıklarının lisanslarını kontrol edin. Bu rehber yalnızca orijinal kaynaklara bağlantı verir; onların kodlarını yeniden lisanslamaz veya aynalamaz.
