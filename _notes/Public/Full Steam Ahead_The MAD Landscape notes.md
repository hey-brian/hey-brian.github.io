---
title: Full Steam Ahead_The MAD Landscape notes
feed: show
date: 2024-04-10
time: 00:36:16
tags: 
comments: true
imageNameKey:
---

## **PART II: 24 THEMES WE’RE THINKING ABOUT IN 2024**

> VC의 [Matt Turck](https://mattturck.com/)의 블로그에서 2024 MAD Landscape 포스팅을 보고, part2를 정리했습니다. 제 관심도에 따라 오역, 오정리가 있을 수 있으니, 관심이 있으시면 꼭 [원글](https://mattturck.com/mad2024/)을 참고해주세요.

### 1. Structured(구조화) vs Unstructured(비구조화) data
1. 구조화 데이터 파이프라인: **행과 열로 정리할 수 있는 데이터입니다.** 구조화 데이터는 BI 툴을 활용해 현재와 과거를 파악하는 '기술 분석'에 사용되며, 전통적인 ML/AI 모델에 투입되어 미래를 '예측 분석'할 때 활용됩니다.
2. 비구조화 데이터 파이프라인: 텍스트, 이미지, 오디오, 비디오 등 **행과 열로 정리하기 어려운 데이터입니다.** 비구조화 데이터는 주로 생성형 AI 모델(LLM 등)을 훈련하고 실행(추론)하는 데 사용됩니다.
현재 ==비구조화 데이터(ML/AI)는 주목받고 있는 반면, 구조화 데이터(Modern Data Stack  등)는 그렇지 않습니다==.

### 2. Modern Data Stack (MDS)의 몰락
- MDS는 기본적으로 위에서 언급한 구조화 데이터 파이프라인을 가리킵니다.
- 2019 ~ 2021년: 소프트웨어 업계에서 Modern Data Stack (MDS)는 '빅데이터'와 함께 최고로 주목 받았습니다.
- Snowflake의 기록적인 IPO로 MDS에 대한 관심이 폭발, 저금리 기조 -> 스타트업 설립,  VC 투자 폭증 -> 데이터 카탈로그, 데이터 관측, ETL, 역ETL 등 여러 범주가 1~2년 만에 과포화 상태 도달

하지만 지금은 상황이 크게 달라졌습니다. ==2023년 MDS가 "압박받고 있다"고 예견했듯이 2024년에 그 압박은 더욱 심화될 전망==입니다.
1. MDS를 구축하려면 여러 벤더의 독립적인 최고 솔루션들을 통합해야 하므로 비용, 시간, 리소스 측면에서 많은 비용이 듭니다. (경기 침체로 예산이 삭감되는 분위기에서 쉽지 않은 투자입니다.)
2. MDS는 더 이상 주목받는 대상이 아닙니다;;;; 생성형 AI가 경영진, VC, 언론의 관심을 모두 사로잡으며, 앞서 언급한 비구조화 데이터 파이프라인이 주목받고 있습니다.

### 3. 데이터 인프라의 통합 및 대기업 확장
2024년 데이터 인프라와 분석 부문에서는 다음과 같은 일이 벌어질 것으로 예상됩니다.
- 많은 Modern Data Stack 관련 스타트업들이 **"AI 인프라 스타트업"으로 적극적으로 재포지셔닝**하고 현대 AI 스택에 자리잡으려 할 것입니다. (대부분은 구조화에서 비구조화 데이터로 전환하려면 근본적인 제품 진화가 필요)
- 데이터 인프라 업계에서 마침내 **통합**이 일어날 것입니다. M&A는 지금까지 제한적이었지만 2023년에 일부 인수합병이 있었습니다. Stemma(Teradata 인수), Manta(IBM 인수), Mode(ThoughtSpot 인수) 등입니다.
- **스타트업 실패가 많아질 것입니다.** VC 투자가 줄어들면서 상황이 어려워졌기 때문입니다. 많은 스타트업이 비용을 대폭 삭감했지만 언젠가는 현금 여력이 바닥날 것입니다.
- 이 분야의 **대기업이나 규모가 큰 기업들**은 플랫폼 전략에 집중하며 기능을 계속 확장할 것입니다. 인수합병으로도 이뤄지겠지만 **자체 개발도 많이 할 것**입니다.

### 4. Databricks vs Snowflake 현황 점검
Snowflake(역사적으로 구조화 데이터 파이프라인 분야 출신)는 여전히 놀라운 기업이며, 가치가 가장 높은 상장 기술주(현재 시가총액/향후 12개월 매출 비율 14.8배) 중 하나입니다. 하지만 다른 소프트웨어 업체들과 마찬가지로 성장세가 크게 둔화되어 2024 회계연도에 전년 대비 38% 제품 매출 성장(26억 7천만 달러)을 기록했고, 현재 기준 향후 12개월 매출 성장률은 22%를 전망하고 있습니다. 무엇보다 **Snowflake는 AI 수용이 더뎠고 인수 합병도 적극적이지 않아 제품 측면에서 압박을 받고 있는 것으로 보입니다.** 최근 CEO 교체도 주목할 만한 대목입니다.
Databricks(역사적으로 비구조화 데이터 파이프라인과 머신러닝 분야 출신)는 전방위적으로 강력한 모멘텀을 보이고 있습니다. 비상장사이지만 2024 회계연도 매출이 16억 달러를 넘어 50% 이상 성장한 것으로 알려졌습니다. 중요한 점은 **Databricks가 MosaicML(13억 달러) 인수를 비롯해 자체 제품 개발로 주요 Generative AI 플레이어로 부상**했다는 것입니다. LLM에 필요한 비구조화 데이터의 주요 저장소이자 Dolly와 최근 발표한 Generative AI 모델 DBRX의 개발사입니다.
Snowflake vs Databricks 경쟁 구도에 새로운 대변수는 **마이크로소프트 Fabric 출시**입니다. 2023년 5월 발표된 이 클라우드 기반 SaaS 플랫폼은 데이터와 분석을 종합적으로 다룹니다. **OneLake, PowerBI, Synapse Data Science 등 마이크로소프트 제품들이 통합되어 데이터 통합/엔지니어링에서 데이터 사이언스까지 모든 워크플로우를 커버**합니다. 대기업 신제품 발표와 실제 제품 간에는 여전히 갭이 있지만, 마이크로소프트의 Generative AI 공세와 함께 위협이 될 수 있습니다. (또한 Databricks는 대부분 Azure 기반이라는 꼬인 사연이 있습니다)

### 5. 2024년 BI와 Generative AI가 데이터 분석을 변화시킬까?
Modern Data Stack 과 구조화 데이터 파이프라인 영역 중에서 **BI(Business Intelligence)는 혁신이 가장 시급한 부문**입니다. (2019년 당시 BI 산업이 거의 완전히 통합되었다고 언급했고, 2021년에는 메트릭 스토어의 등장을 다뤘습니다.)
그러나 **BI/분석의 변화 속도는 예상보다 더뎠습니다.** 마이크로소프트 파워BI, 세일즈포스 테이블로, 구글 루커 등 기존 제품들이 여전히 지배적입니다. 통합 계약을 통해 무료로 제공되기도 합니다. ThoughtSpot이 Mode를 인수하고 Sisu는 Snowflake에 인수되는 등 일부 통합이 있었습니다. dbt(semantic layer/MetricFlow), Trace(metrics tree)) 등 혁신적인 접근을 시도하는 스타트업도 있지만 여전히 초기 단계입니다.
데이터 추출과 변환 측면에서 Generative AI가 강력한 역할을 할 수 있을 뿐 아니라 데이터 분석 자체를 대중화하고 힘을 실어줄 수 있습니다.
관련 활동이 많이 이루어졌습니다. OpenAI는 Code Interpreter(현 Advanced Data Analysis)를 출시했고, 마이크로소프트는 Excel용 Copilot AI 채팅봇을 내놨습니다. 클라우드 벤더, Databricks, Snowflake, 오픈소스, ==많은 스타트업들이 자연어로 데이터베이스 쿼리를 실행할 수 있는 "Text to SQL" 제품 개발에 박차를 가하고 있습니다==.
이는 매력적이면서도 파괴적일 수 있습니다. 데이터 분석의 지상 과제는 대중화입니다. 자연어 인터페이스가 노트북, 데이터베이스, BI 툴의 인터페이스가 된다면 훨씬 더 많은 사람이 분석을 할 수 있게 됩니다.
하지만 BI 업계에서는 회의적인 시각도 있습니다. SQL의 정확성과 쿼리 배경이 되는 비즈니스 맥락 이해의 미묘함이 자동화의 큰 장애물로 여겨지기 때문입니다.

### 6. 현대 AI 스택의 부상
언급했듯이 비구조화 데이터 인프라는 전혀 다른 상황에 놓여 있습니다. **비구조화 데이터가 LLM을 공급하고 있으며, 이에 대한 수요가 폭발적입니다.** Generative AI를 실험하거나 배포하는 모든 기업이 오래된 격언을 새삼 발견하고 있습니다. "데이터가 새로운 석유다". 모두가 LLM의 힘을 원하지만, 자사(기업) 데이터를 통해 학습된 모델을 원합니다.
대기업, 중소기업 할 것 없이 Generative AI 인프라 시장 기회를 향해 몰려들고 있습니다.
Databricks를 비롯한 여러 AI 스케일업 기업들이 시장 모멘텀을 잡기 위해 적극적으로 제품을 진화시키고 있습니다. Scale AI는 원래 자율주행차 시장을 위해 개발한 레이블링 인프라를 OpenAI 등과 협력하여 기업 데이터 파이프라인으로 진화시켰습니다. Dataiku는 LLM Mesh를 출시해 글로벌 2000대 기업이 여러 LLM 벤더와 모델을 원활하게 활용할 수 있게 했습니다.
한편 다음과 같은 분야에서 새로운 세대의 AI 인프라 스타트업들이 부상하고 있습니다.
- Vector databases: Generative AI 모델이 소비할 수 있는 형식(벡터 임베딩)으로 데이터를 저장합니다. Pinecone, Weaviate, Chroma, Quadrant 등의 전문 업체들이 전성기를 구가했고, MongoDB 같은 기존 DB 업체도 벡터 검색 기능을 추가했습니다.
- Frameworks: LlamaIndex, Langchain 등이 여러 구성요소를 연결하고 조율합니다.
- Guardrails: LLM과 사용자 사이에 위치해 모델 출력이 조직 규칙을 준수하도록 합니다.
- Evaluators: 공개 벤치마크에 대한 불신으로 인해 Generative AI 모델 성능 테스트, 분석, 모니터링이 어려운 문제를 해결합니다.
- Routers: 실시간으로 성능, 비용, 사용자 경험을 최적화하기 위해 사용자 쿼리를 다양한 모델에 분산시킵니다.
- Cost guards: LLM 사용 비용을 모니터링합니다.
- Endpoints: 기반 인프라(모델 등)의 복잡성을 추상화한 API 입니다.
Modern Data Stack 의 역사로 인해 "현대 AI 스택"이라는 용어 사용을 주저했습니다.
하지만 이 표현은 많은 유사점을 잘 포착하고 있습니다. 이들 스타트업도 과거 MDS 기업들처럼 '핫 기업'이며, 마케팅 제휴와 제품 파트너십을 맺으며 '무리를 지어' 다닙니다.
또한 이 새로운 AI 인프라 스타트업들도 이전 MDS 기업들이 직면했던 몇 가지 과제에 부딪힐 것입니다. 이들 범주 중 어느 것이 수십억 달러 기업을 만들 만큼 충분히 큰지, 어떤 부분을 대기업들(주로 클라우드 업체지만 Databricks, Snowflake도)이 자체 개발할지 등입니다.

### 7. AI 과열 주기 현황은?
AI에는 수십 년에 걸친 AI 전성기와 AI 겨울의 역사가 있습니다. 지난 10-12년 동안에만 세 번째 AI 과열 주기를 겪고 있습니다. 2012년 ImageNet 이후 딥러닝이 주목받으며 2013-2015년 한차례, 채팅봇 열풍과 TensorFlow의 부상으로 2017-2018년경 또 다른 주기가 있었고, 2022년 11월 Generative AI가 등장하며 지금의 과열기를 맞이하고 있습니다.
이번 과열기는 AI 거품 분위기일 정도로 특히 극심했는데, 그 이유는 다음과 같습니다. **기술 자체가 매우 인상적이고, 기술 분야 밖의 광범위한 대중에게도 와닿으며, 다른 기술 분야가 침체기에 빠진 가운데 VC들에게는 유일한 투자처였기 때문입니다**.
과열기는 상반된 효과를 가져왔습니다. 긍정적으로는 "도전적 프로젝트를 위한 자금 확보"와 "1000개의 꽃이 피어나는" 기회가 열렸습니다. 부정적으로는 일회성 AI 전문가와 스타트업 난립, 과도한 AI 컨퍼런스/팟캐스트/뉴스레터, 너무 많은 AI 생태계 지도 등 지나친 소음이 발생했습니다.
과열기의 주요 문제는 불가피한 반발(inevitable blowback)입니다.
이 단계에는 상당한 "기현상과 위험"(“quirkiness” and risk built into this market phase)이 내재되어 있습니다. 선두 기업의 매우 이례적인 법적, 지배구조 체계, 잘 이해되지 않거나 공개되지 않는 "지분 대가 컴퓨팅 자원" 거래, AI 연구원 팀에 의해 운영되는 많은 유망 스타트업, ZIRP(제로금리) 시절을 연상케 하는 VC 딜 (선점 경쟁, 큰 라운드, 초기 기업에 대한 astronomic한 기업가치 평가) 등입니다.
AI 과열 분위기에 금이 가기는 했지만(다음 참조), 매주 새로운 것이 모두를 깜짝 놀라게 하는 국면입니다. 사우디아라비아의 400억 달러 AI 펀드 설립 소식 등에서 보듯 이 분야로의 자금 유입이 당분간 계속될 전망입니다.

### 8. 실험 vs 현실: 2023년은 가상의 해프닝이었나?
과열 분위기에 비춰볼 때, 지금까지 실제 사례와 단순 실험은 어느 정도였을까요?
2023년은 역동적인 한 해였습니다. a) 모든 기술 업체가 Generative AI를 제품에 통합하려 했고 b) 모든 글로벌 2000대 기업 이사회가 팀에 "AI 도입" 지시를 내렸으며 일부 기업에서 모건스탠리, 시티은행 등 규제 산업에서도 빠른 속도로 기업 배포가 이뤄졌고 c) 물론 소비자들도 Generative AI 앱에 열렬한 관심을 보였습니다.
결과적으로 2023년에는 큰 성과가 있었습니다. OpenAI는 연간 20억 달러 수익을 달성했고, Anthropic은 2024년 8억 5천만 달러 매출을 전망할 만큼 성장했으며, Midjourney는 투자 없이 40명의 팀으로 2억 달러 매출을 올렸고, Perplexity AI는 출범 1년 만에 1천만 명의 월간 활성 사용자를 확보했습니다.
그렇다면 회의적 시각도 필요할까요? 우려되는 점은 다음과 같습니다.
- 기업에서 많은 지출이 PoC나 간단한 성과에 집중되었고 대부분 혁신 예산에서 나왔습니다.
- **실제 비즈니스 문제 해결보다는 경영진의 뒤처짐 방지 의지(not appear flat-footed)가 더 컸을 수 있습니다.**
- 소비자 AI 앱에는 높은 이탈률이 있습니다. 단순 호기심에 그쳤을 수 있습니다.
- 개인적으로나 직업적으로 많은 이들이 Generative AI 앱과 제품을 제대로 활용하기 어려웠다고 합니다.
- 최고 AI 전문가들이 만든 Generative AI 제품도 모두 마법 같지는 않을 것입니다. 13억 달러 투자 후 Inflection AI가 빨리 접었다면, 세상이 또 다른 AI 챗봇이나 LLM 공급업체를 더는 필요로 하지 않는다는 인정이었을지 모릅니다.

### 9. LLM 기업들: 결코 대체재가 되지 않을까?
수십억 달러의 벤처캐피탈과 기업 자금이 기초 모델 기업에 투자되고 있습니다.
따라서 지난 18개월간 가장 많이 논의된 질문: 우리는 궁극적으로 대체재가 될 제품에 엄청난 자본 소각을 목격하고 있는 것일까요? 아니면 그 LLM 공급업체들이 새로운 AWS, Azure, GCP가 되는 것일까요?
**우려되는 사실(해당 기업들에게)은 어떤 LLM도 지속 가능한 성능 우위를 구축하지 못하고 있다는 점입니다.** 현재 Claude 3 Sonnet과 Gemini Pro 1.5가 GPT-4보다 우수하고, GPT-4가 Gemini 1.0 Ultra보다 낫지만, 이런 순위는 몇 주마다 바뀝니다. ChatGPT의 성능도 한때 "정신 나갔다" "게을러졌다"가 있었습니다.
게다가 오픈소스 모델(Llama 3, Mistral, DBRX 등)의 성능이 빠르게 따라잡고 있습니다.
별도로 - 예상보다 훨씬 더 많은 LLM 공급업체들이 시장에 있습니다. 몇 년 전만 해도 승자독식 구도에서 1-2개 LLM 기업만 존재할 것이라는 게 통설이었습니다. 트랜스포머를 확장할 수 있는 전문성을 갖춘 인력이 전 세계적으로 소수에 불과했기 때문입니다.
하지만 예상보다 더 많은 유능한 팀이 있었습니다. OpenAI, Anthropic 외에도 Mistral, Cohere, Adept, AI21, Imbue, 01.AI 등 많은 스타트업이 기초 AI 작업을 수행하고 있고, 구글, 메타 등 대기업 팀들도 있습니다.
그렇지만 지금까지 LLM 공급업체들은 잘 나가는 편입니다. OpenAI와 Anthropic의 매출은 엄청난 속도로 성장하고 있습니다. LLM 모델은 대체재가 될지 모르겠지만, LLM 기업에겐 여전히 엄청난 기회가 있습니다. 이들은 이미 기저 모델 외에도 소비자, 기업, 개발자 등 다양한 대상에 애플리케이션과 도구를 제공하는 "풀스택" 기업이 되었습니다.
아마도 클라우드 벤더와의 비유가 적절할 것입니다. AWS, Azure, GCP도 애플리케이션/도구 계층으로 고객을 유치·유지하고, 대부분 차별화되지 않은 컴퓨팅/스토리지 계층으로 수익을 창출하고 있습니다.

### 10. LLM, SLM 그리고 하이브리드 미래
대규모 언어 모델(LLM)에 대한 열기가 있는 반면, **최근 몇 달간 분명한 추세는 소규모 언어 모델(SLM)의 가속화입니다.** 메타의 Llama-2-13b, Mistral의 Mistral-7b와 Mixtral 8x7b, 마이크로소프트의 Phi-2와 Orca-2 등이 대표적입니다.
LLM이 점점 더 커지고 있지만(GPT-3는 1750억 개 파라미터, GPT-4는 1조 7천억 개 파라미터라고 하며, 더 거대한 GPT-5를 기다리고 있습니다), SLM은 많은 사용 사례에서 강력한 대안이 되고 있습니다. 운영 비용이 저렴하고 파인튜닝이 쉬우며 종종 뛰어난 성능을 제공하기 때문입니다.
또 다른 가속화 추세는 **코딩(Code-Llama, Poolside AI) 또는 특정 산업(블룸버그의 금융 모델, 소재과학 전문 Orbital Materials 등)에 특화된 특수 모델의 부상**입니다.
이미 여러 기업 배포 사례에서 볼 수 있듯이, 세상은 빠르게 다중 모델을 결합한 하이브리드 아키텍처로 진화하고 있습니다.
가격이 하락하고는 있지만(아래 참조) 대형 독점 LLM은 여전히 매우 비쌉니다. 지연 시간 문제도 있습니다. 따라서 고객/사용자들은 점점 더 특정 요구 사항과 비용 제약에 맞춰 대형/소형, 상용/오픈소스, 범용/특수 등 다양한 모델 조합을 배포하게 될 것입니다.

### 11. 전통적 AI는 죽었는가?
ChatGPT 출시 이후 재미있는 일이 벌어졌습니다. 기존에 배포되었던 AI 대부분이 하룻밤 사이에 "전통적 AI"로 분류되었습니다. 이는 "Generative AI"와 대비되는 개념입니다.
"전통적"이라는 단어가 새로운 AI에 의해 기존 AI가 완전히 대체될 것을 시사하므로, 당시 최첨단 작업을 수행하던 많은 AI 실무자와 기업에게 충격이었습니다.
그러나 실제로는 훨씬 더 미묘한 상황입니다. **전통 AI와 Generative AI는 궁극적으로 서로 보완적입니다.** 다른 유형의 데이터와 사용 사례를 다루기 때문입니다.
"전통 AI" 또는 가끔 "예측 AI" 혹은 "테이블 AI"라고 불리는 것도 현대 AI(딥러닝 기반)의 일부분입니다. 다만 일반적으로 구조화된 데이터(위 참조)와 추천, 이탈 예측, 가격 최적화, 재고 관리 등의 문제에 초점을 맞춥니다. 전통 AI는 지난 10년간 엄청난 도입을 경험했으며, 이미 전 세계 수천 기업에서 대규모로 실제 운영 중입니다.
반면 Generative AI는 주로 비구조화 데이터(텍스트, 이미지, 비디오 등)를 다룹니다. 코드 생성, 이미지 생성, 검색 등 다른 유형의 문제를 매우 잘 해결합니다.
여기서도 **미래는 하이브리드입니다.** 기업들은 특정 작업에 LLM을, 다른 작업에는 예측 모델을 사용할 것입니다. 가장 중요한 것은 이들을 종종 결합할 것이라는 점입니다. LLM이 이탈 예측과 같은 정확한 예측을 잘하지 못할 수 있지만, 해당 예측을 제공하는 다른 모델의 출력을 활용하는 LLM을 사용할 수 있습니다. 반대의 경우도 마찬가지입니다.

### 12. 얇은 래퍼, 두꺼운 래퍼 그리고 풀스택 경쟁
"얇은 래퍼"는 2023년 모두가 사용하던 경멸적인 용어였습니다. 핵심 역량이 타사 기술(예: OpenAI)에 의존한다면 장기적인 가치와 차별화를 만들기 어렵다는 주장입니다. 그리고 매출 급증 이후 Jasper 같은 스타트업들이 어려움을 겪었다는 최근 보도는 이런 생각을 뒷받침합니다.
흥미로운 질문은 신생 스타트업들이 더 많은 기능을 구축해나가면서 시간이 지날수록 어떤 일이 일어날지 입니다. 얇은 래퍼가 두꺼운 래퍼로 변할 수 있을까요?
2024년 현재로서는 두꺼운 래퍼가 다음과 같은 방식으로 차별화할 수 있는 길이 있는 것 같습니다.
- 특정 문제, 종종 특정 수직 분야에 집중함. 너무 수평적이면 빅테크의 "킬존"에 들어갈 위험이 있습니다.
- 그 문제에 특화된 워크플로우, 협업, 심층 통합 기능을 구축합니다.
- AI 모델 수준에서 많은 작업을 수행합니다. 특정 데이터셋으로 모델 파인튜닝하거나 특정 비즈니스에 맞춘 하이브리드 시스템(LLM, SLM 등)을 만듭니다.
즉, 좁고 '풀스택'(애플리케이션과 인프라 모두)이어야 할 것입니다.

### 13. 2024년 주목할 만한 분야: AI 에이전트, 에지 AI
지난 1년간 AI 에이전트 개념에 대한 관심이 많았습니다. 기본적으로 작업을 수행할 수 있는 지능형 시스템의 최종 단계이며, 종종 협력적인 방식으로 작동합니다. 여행 예약 보조(소비자 사례)부터 전체 SDR 캠페인 자동화(생산성 사례), RPA 스타일 자동화(기업 사례)까지 다양합니다.
AI 에이전트는 자동화의 꿈입니다. "텍스트에서 행동으로" 패러다임으로, AI가 우리를 대신해 일을 처리합니다.
몇 달마다 AI 세계는 BabyAGI, Devin AI(AI 소프트웨어 엔지니어) 등 에이전트 같은 제품에 열광합니다. 하지만 대체로 이런 흥분은 시기상조인 것으로 입증되었습니다. 복잡한 여러 모델 시스템이 협력하여 실제 행동을 수행하려면 먼저 Generative AI를 견고하고 예측 가능하게 만드는 많은 작업이 필요합니다. 메모리 등 부족한 구성요소도 있습니다. 그러나 **앞으로 1~2년 안에 AI 에이전트 분야가 특히 주목받을 것으로 예상됩니다**.
또 다른 흥미로운 분야는 **Edge AI**입니다. 대규모로 운영되고 엔드포인트로 제공되는 LLM에 거대한 시장이 있지만, **AI의 꿈은 GPU 없이 휴대폰, 지능형 IoT 기기 등 로컬 디바이스에서 구동되는 모델**이었습니다. 이 분야는 매우 활발합니다: Mixtral, Ollama, Llama.cpp, Llamafile, GPT4ALL(Nomic) 등. 구글과 애플도 점점 더 적극적일 것으로 보입니다.

### 14. Generative AI가 AGI를 향해 가는가, 아니면 정체기를 맞이하는가?
매주 놀라운 새 제품이 등장하는 가운데 AI에 대한 열렬한 평가들을 고려할 때 이는 거의 신성모독 질문일 수 있습니다. 그렇지만 AGI에 이르기보다는 Generative AI의 진전이 더딘 세계가 있을 수 있을까요? 그렇다면 그 의미는 무엇일까요?
두 가지 주장이 있습니다. 첫째, 기초 모델은 브루트포스 연산(brute force exercise)이므로 궁극적으로 이를 공급할 자원(컴퓨팅, 데이터)이 고갈될 것이고, 둘째, AGI로 가는 길은 추론 능력인데 LLM은 이를 할 수 없습니다.
흥미롭게도 이는 2018년 당시 업계에서 이뤘던 논의와 비슷합니다. **2018년 이후 주된 변화는 (점점 더 발전된) 모델에 막대한 데이터와 컴퓨팅 파워를 투입한 것뿐입니다.**
AI 추론 능력이 얼마나 진전되었는지는 덜 분명합니다. 다만 DeepMind의 AlphaGeometry는 언어 모델과 논리 규칙을 활용한 기호 엔진을 결합해 중요한 이정표가 되었습니다.
컴퓨팅 및 데이터 자원의 한계에 얼마나 가까웠는지는 평가하기 어렵습니다. 컴퓨팅 한계에 대한 우려는 하루가 다르게 물러나고 있습니다. 최근 발표된 NVIDIA Blackwell GPU 시스템으로 270조 개 파라미터 모델(GPT-4는 1.7조 개)을 구축할 수 있게 되었습니다.
데이터 문제는 복잡합니다. 합법적인 라이선스 데이터 고갈(OpenAI 라이선스 딜 참고) 문제도 있지만, 전반적인 텍스트 데이터 부족 문제도 있습니다. 합성 데이터에 대한 작업이 많이 진행 중입니다. Yann LeCun은 다음 단계 모델을 만들려면 더 풍부한 비디오 데이터를 소화할 수 있어야 한다고 말했습니다.
GPT-5에 대한 기대가 엄청납니다. GPT-4보다 얼마나 낫느냐가 AI 발전 속도의 바로미터로 폭넓게 인식될 것입니다.
스타트업 생태계 관점(창업가, 투자자)에서 본다면, 중기적으로는 Generative AI 진전이 지금 정체된다고 해도 문제가 덜할 수 있습니다. **현재 기술로도 수직/사례를 가로지르며 수년간 사업 기회가 있기 때문입니다**.

### 15. GPU 전쟁 (NVIDIA는 과대평가 되었나?)
우리는 컴퓨팅 파워가 세상에서 가장 귀중한 자원이 되는 거대한 주기의 초기에 있는지, 아니면 곧 큰 붕괴를 맞이할 GPU 생산 과잉 단계인지 모르겠습니다.
생성 AI 지원 GPU 분야의 사실상 유일한 존재인 NVIDIA는 엄청난 전성기를 누리고 있습니다. 주가가 5배 상승해 2.2조 달러 평가액을 기록했고, 2022년 말 이래 총매출이 3배 증가했습니다. 실적 발표와 젠슨 황 CEO의 GTC 행사는 2024년 최대 행사인 테일러 스위프트 콘서트 수준의 열기를 보였습니다.
이는 부분적으로 VC들이 AI에 수십억 달러를 투자한 최종 수혜자였기 때문일 수 있습니다.
그 어떤 기업으로서의 탁월함에도 불구하고, NVIDIA의 운명은 현재 붐이 얼마나 지속 가능한지에 달려 있습니다. 하드웨어 사업은 어렵고, 대만 TSMC에서 정확히 얼마나 많은 GPU를 생산해야 하는지 예측하기는 힘듭니다.
AMD, 인텔, 삼성 등 경쟁사들도 반격을 가하고 있고, Groq나 Cerebras 등 스타트업들도 가속화하고 있으며, 샘 알트먼의 7조 달러 칩 회사 설립 루머에서 보듯 새로운 기업이 생길 수도 있습니다. 구글, 인텔, 퀄컴 등 기술 기업 연합체도 NVIDIA의 비밀 무기인 CUDA 소프트웨어를 공략하고 있습니다.
GPU 부족 사태가 가라앉으면 단기-중기적으로 NVIDIA에 하방 압력이 가해질 수 있지만, **장기적으로 AI 칩 제조사들의 전망은 여전히 밝습니다.**

### 16. 오픈소스 AI: 지나친 혜택인가?
이번 주제는 약간의 논란을 일으키려는 의도가 있습니다. 저는 오픈소스 AI의 큰 팬이며, 지난 1년여 동안 이것이 주요 트렌드였음은 분명합니다. 메타는 Llama 모델을 대거 공개했고, 프랑스의 Mistral은 논란의 대상에서 생성 AI의 새로운 스타로 부상했으며, 구글은 Gemma를 출시했습니다. 또한 HuggingFace는 수많은 모델을 호스팅하며 오픈소스 AI의 활기찬 본거지로 자리매김했습니다. 생성 AI 분야에서 가장 혁신적인 작업들이 오픈소스 커뮤니티에서 이뤄졌습니다.
**하지만 동시에 오픈소스 커뮤니티에 인플레이션 분위기가 만연해 있다는 일반적인 느낌도 있습니다.** 수십만 개의 오픈소스 AI 모델이 지금 공개되어 있습니다. 많은 모델이 장난감이나 주말 프로젝트에 불과합니다. 모델들이 랭킹에서 오르내리며, 일부는 GitHub 스타 기준(지표로는 결함이 있지만)으로 단 며칠 만에 유례없는 인기를 끌다가도 별다른 실용성 없이 사라집니다.
성공적인 오픈소스 프로젝트에 대한 파워로 분포로 인해 시장은 자체 조정될 것입니다. 그리고 클라우드 공급업체와 기타 대기업의 지원이 몰릴 것입니다. 하지만 그 동안의 폭발적인 증가는 많은 사람들에게 어지러움을 안겨주었습니다.

### 17. 실제 AI 비용은 얼마일까?
생성 AI의 경제성은 빠르게 진화하는 주제입니다. 그리고 놀랍지 않게도 이 분야의 미래는 경제성에 많이 달려 있습니다. 예를 들어 AI 기반 답변 제공 비용이 10개의 파란색 링크 제공 비용보다 훨씬 높다면 구글의 검색 서비스를 제대로 대체할 수 있을까요? 또한 추론 비용이 총이익의 상당 부분을 차지한다면 소프트웨어 기업이 진정으로 AI 기반이 될 수 있을까요?
다행히도 AI 모델의 고객/사용자 입장에서는 가격 인하 경쟁이 예상보다 빨리 시작된 초기 단계인 것 같습니다. 주요 동인은 Mistral 등 오픈소스 AI와 Together AI, Anyscale, Replit 등 오픈 모델을 엔드포인트로 제공하는 상업용 추론 벤더의 동시 부상입니다. 고객 입장에서 전환 비용이 거의 없어(다른 모델에서 다른 결과가 나오는 복잡성은 제외하고) OpenAI와 Anthropic에 압박이 가해지고 있습니다. 이는 OpenAI, Together AI 등 다수 벤더가 동시에 임베딩 모델 가격을 크게 인하한 데서 볼 수 있습니다.
하지만 벤더 관점에서 **AI 구축 및 제공 비용은 여전히 매우 높습니다**. Anthropic은 수익의 절반 이상을 AWS, GCP 등 클라우드 업체에 LLM 운영 비용으로 지출한 것으로 알려졌습니다. 출판사와의 라이선스 계약 비용도 듭니다.
### 18. AI의 정치경제학 변화와 대기업: 마이크로소프트가 승리했나?
2022년 말부터 모두가 던졌던 질문 중 하나이며, 2024년에도 매우 주목받고 있습니다. 대기업이 생성 AI의 대부분 가치를 차지하게 될 것인가?
**AI는 규모의 경제를 누립니다. 더 많은 데이터, 컴퓨팅 파워, AI 연구원이 더 큰 능력을 낳는 경향이 있죠.** 대기업들은 이를 잘 인식하고 있습니다. 과거 플랫폼 전환기의 기존 업체들과 달리 앞으로 다가올 혁신에 대해 매우 민첩하게 대응하고 있습니다.
대기업 중에서도 마이크로소프트는 4차원 체스를 두는 것 같습니다. 2019년 OpenAI에 최초 투자한 것을 포함해 현재까지 130억 달러를 투자했습니다. 하지만 오픈소스 경쟁사 Mistral과도 협력했습니다. ChatGPT 라이벌 Inflection AI에 투자했다가 최근 인수까지 단행했습니다.
결국 이런 파트너십은 마이크로소프트의 클라우드 컴퓨팅 수요를 더욱 키웠습니다. Azure 매출이 전년 대비 24% 증가한 330억 달러를 기록했으며, 그중 6%p는 AI 서비스 덕분이었습니다.
반면 구글과 아마존은 OpenAI의 경쟁사 Anthropic와 협력하고 투자했습니다. (현재 아마존이 40억 달러 투자 계획 중 27억 5천만 달러를 2차로 투입했습니다) 아마존은 오픈소스 Hugging Face와도 협력했고, 구글과 애플은 Gemini AI를 애플 제품에 탑재하는 방안을 논의 중입니다. 메타는 오픈소스 AI에 올인하며 다른 기업들을 위협하고 있습니다. 중국에서도 여러 움직임이 있습니다.
당연한 질문은 스타트업이 성장하고 성공할 여지가 얼마나 있는가입니다. OpenAI, Anthropic 등 1군 스타트업은 적절한 파트너십을 맺고 탈출 속도에 올랐습니다. Mistral도 가까운 시일 내 합류할 수 있겠죠. 하지만 자금력이 좋은 다른 스타트업들의 행방은 여전히 불투명합니다.
Inflection AI의 인수 결정과 Stability AI CEO 교체 등에서 "2군" 생성 AI 스타트업 그룹의 상업적 진전이 어려웠음을 읽을 수 있을까요?

### 19. OpenAI에 그저 열광하고 있는 걸까요?
OpenAI에 대한 관심이 계속해서 증가하고 있습니다. 860억 달러의 평가 가치, 수익 성장, 궁정 드라마, 그리고 Sam Altman이 이 세대의 Steve Jobs로 여겨지고 있습니다. 몇 가지 흥미로운 질문들이 있습니다.
1. OpenAI가 너무 많은 일을 시도하고 있는가? 11월 드라마 이전에, OpenAI는 AI의 모든 것을 수직적(전체 스택)과 수평적(사례별 사용)으로 다루겠다는 것을 분명히 했습니다: 모델 + 인프라 + 소비자 검색 + 기업 + 분석 + 개발 도구 + 마켓플레이스 등. 이는 초기 리더가 큰 패러다임 변화에서 무제한적인 자본 접근을 가질 때 보이는 전략이지만, 경쟁이 치열해진 상황에서 실행하기에는 상당한 도전이 될 것입니다.
2. OpenAI와 Microsoft가 결별할까요? Microsoft와의 관계는 흥미롭습니다 - Microsoft의 지원은 OpenAI에게 자원(컴퓨트 포함)과 배포(Azure in the enterprise) 측면에서 큰 도움이 되었으며, 초기 Generative AI 웨이브에서 Microsoft의 탁월한 움직임으로 평가되었습니다. 동시에, **Microsoft는 OpenAI에 의존하지 않음을 분명히 했으며, 경쟁사와 파트너십을 맺고, Inflection AI 인수를 통해 AI 연구 팀을 대폭 강화했습니다**.
OpenAI가 Microsoft와의 파트너십에 단일 스레드로 남고 싶어할지, 아니면 다른 클라우드에 배포되길 원할지 궁금합니다. OpenAI의 거대한 야망과 Microsoft의 글로벌 지배를 목표로 할 때, 양사가 경쟁자보다는 파트너라는 결론을 내릴 시점은 언제일까요?

### 20. 2024년은 AI회사들의 한 해가 될까요?
2023년은 기업에서 새로운 트렌드를 받아들이려는 시도가 많았지만, 실제로는 몇 가지 개념 증명을 제외하고는 큰 변화가 없는 해였습니다.
**Generative AI 분야에서 2023년 가장 큰 승자는 AI 컨설팅으로 20억 달러의 수익을 창출한 것으로 보고된 Accenture와 같은 회사들이었습니다.** 그럼에도 불구하고, 2024년이 기업에서 AI, 특히 Generative AI에 있어 큰 해가 될 것이라는 희망이 큽니다.
하지만 우리는 아직 Global 2000 유형의 회사들이 직면한 몇 가지 핵심 질문에 대한 답을 찾는 초기 단계에 있습니다:
1. 사용 사례는 무엇인가? 쉽게 달성할 수 있는 사용 사례(The low hanging fruit use cases)는 다음과 같습니다. a) 개발 팀을 위한 코드 생성 co-pilots, b) 기업 지식 관리(검색, 텍스트 요약, 번역 등), c) 고객 서비스를 위한 AI 챗봇(Generative AI 이전부터 있는 사용 사례) 등이었습니다.
2. 어떤 도구를 선택해야 하는가? 상**업 벤더와 오픈 소스, 크고 작은 모델, 수평적 및 수직적 GenAI 도구의 조합인 하이브리드 미래가 예상됩니다**.
3. 도구를 배포하고 유지 관리할 사람은 누구인가? Global 2000 회사들 사이에는 분명한 기술 부족이 있습니다.
4. 그들이 환상(_hallucinate_)을 보지 않도록 어떻게 할 것인가? RAG와 가드레일, 평가 등 주변에서 많은 작업이 이루어지고 있지만, **Generative AI 도구가 완전히 틀릴 수 있고, 우리가 Generative AI 모델이 어떻게 작동하는지 정말로 모른다는 더 큰 문제가 있습니다**.
5. ROI는 무엇인가? 대형 기술 회사들은 자신들의 필요에 맞게 Generative AI를 조기에 활용하기 시작했으며, 흥미로운 초기 데이터를 보여주고 있습니다.
Generative AI 벤더에게 좋은 소식은 기업 고객들이 예산(**중요하게도 더 이상 "혁신" 예산이 아니라 실제 OpEx 예산**)과 자원을 할당하는 데 많은 관심이 있다는 것입니다. 그러나 우리는 아마도 1년이 아닌 3-5년의 배포 주기에 대해 이야기하고 있을 것입니다.

### 21.  AI는 SaaS를 제거하게 될까요?
지난 12개월 동안 유행한 아이디어 중 하나는 AI가 SaaS를 종말로 이끌 것인가 하는 것이었습니다.
이 질문의 한 버전은 AI가 코딩을 10배 더 쉽게 만들어서, 몇 명의 평균적인 개발자만 있으면 사용자의 필요에 맞춘 맞춤형 SaaS 제품을 만들 수 있다는 것입니다. 자신만의 것을 만들 수 있다면 왜 많은 돈을 SaaS 제공업체에 지불해야 할까요?
또 다른 종류의 질문은 미래는 여러 모델로 구성될 수 있는 하나의 AI 지능이 회사 전체를 운영하는 에이전트 시리즈와 함께하는 것입니다. AI 지능이 모든 것을 완전 자동화되고 매끄러운 방식으로 처리하기 때문에 **더 이상 HR 소프트웨어, 재무 소프트웨어, 판매 소프트웨어를 구매할 필요가 없습니다**.
우리는 이러한 추세가 어떤 식으로든 완전히 실현되는 것에서 다소 멀어 보이지만, 우리 모두 알다시피 AI에서는 변화가 매우 빠르게 일어납니다.
그 사이에, SaaS 제품이 AI가 각각에 내장됨에 따라 더욱 강력해질 것이라는 미래의 가능성이 높아 보입니다.

### 22. AI는 벤처 캐피탈을 없앨까요?
AI가 벤처 캐피탈을 자동화할 수 있는지에 대한 흥미로운 주제를 제쳐두고, AI 플랫폼 전환에 대한 자산 클래스의 적절한 규모에 대한 여러 질문이 있습니다:
벤처 캐피탈은 너무 작은가? OpenAI와 같은 회사들은 수십억 달러를 모금해야 했으며, 앞으로 더 많은 자금이 필요할 수 있습니다. 이러한 자금의 많은 부분은 Microsoft와 같은 대기업에 의해 제공되었을 가능성이 크며, 대부분 compute-for-equity 거래의 형태일 것입니다. **물론 많은 벤처 캐피탈이 큰 기초 모델 회사에 투자했지만, 이러한 투자는 전통적인 VC 소프트웨어 투자 모델에서 명확한 이탈을 나타냅니다**. 아마도 AI 투자는 메가 사이즈의 VC 펀드를 요구할 것입니다 - 작성 시점에, 사우디아라비아는 미국 VC 회사들과 협력하여 400억 달러 규모의 AI 펀드를 출범시킬 예정으로 보입니다.
벤처 캐피탈은 너무 큰가? AI가 우리의 생산성을 10배 향상시키고, 슈퍼 코더와 자동화된 SDR 에이전트, 자동화된 마케팅 생성을 포함한다고 믿는다면, 우리는 곧 수백만 달러의 수익을 창출하고 공개될 수 있는 (아마도 단 한 명의 솔로프레너에 의해 운영되는) 완전 자동화된 회사들의 세대를 목격하게 될 것입니다. 솔로프레너에 의해 운영되는 1억 달러 ARR 회사는 여정의 어느 시점에서든 벤처 캐피탈이 필요한가요?

### 23. AI는 소비자 시장을 부활시킬까요?
소비자 시장은 소셜 미디어와 모바일 시대 이후 다음 돌풍을 찾고 있었습니다. Generative AI는 그 해답이 될 수 있습니다.
몇 가지 흥미로운 분야(그 외 많은 분야 중에서):
1. 검색: 수십 년 만에 처음으로, Google의 검색 독점에 초기 단계이지만 신뢰할 수 있는 경쟁자들이 나타났습니다. Perplexity AI와 You.com과 같은 몇몇 스타트업들이 검색 엔진에서 답변 엔진으로의 진화를 이끌고 있습니다.
2. AI 동반자: 디스토피아적인 측면을 넘어서, 모든 인간이 지식, 엔터테인먼트, 치료 등 특정 필요에 맞춰 무한히 인내심 있고 도움이 되는 동반자를 가질 수 있다면 어떨까요?
3. AI 하드웨어: Humane, Rabbit, VisionPro와 같은 소비자 하드웨어 분야의 흥미로운 신규 진입 기업들이 있습니다.
4. 하이퍼-개인화된 엔터테인먼트: Generative AI 기반 도구가 계속해서 개선되고 (그리고 저렴해지면서) 우리가 발명할 새로운 엔터테인먼트와 예술 형태는 무엇일까요?

### 24. AI와 blockchain: BS, or exciting?
AI와 암호화폐의 교차점은 X/Twitter 농담의 완벽한 소재처럼 느껴질 수 있습니다.
그러나 AI가 가장 많은 컴퓨팅 파워, 데이터, AI 인재를 보유한 소수의 회사에 집중되고 있다는 것은 부인할 수 없는 우려입니다. 이는 Big Tech부터 유명하게도 '열린' 것이 아닌 OpenAI에 이르기까지 다양합니다. 한편, 블록체인 제안의 핵심은 참여자들이 자원과 자산을 공유할 수 있는 분산 네트워크의 생성을 가능하게 하는 것입니다. 여기에는 탐색할 가치가 있는 비옥한 땅이 있으며, 몇 년 전부터 우리가 탐색하기 시작한 주제입니다.
Bittensor*(분산형 기계 지능 플랫폼), Render(분산형 GPU 렌더링 플랫폼), Arweave(분산형 데이터 플랫폼)을 포함한 여러 AI 관련 암호화폐 프로젝트가 눈에 띄는 가속을 경험했습니다.
올해의 MAD Landscape에 암호화폐 섹션을 포함시키지 않았지만, 이는 주목할 만한 분야입니다.
이제, 항상 그렇듯이, 문제는 암호화폐 산업이 스스로를 도울 수 있을지, 그리고 수백 개의 AI 관련 메메코인, 펌프 앤 덤프 계획, 사기로 퇴화하지 않을지 여부입니다.

> VC의 [Matt Turck](https://mattturck.com/)의 블로그에서 2024 MAD Landscape 포스팅을 보고, part2를 정리했습니다. 제 관심도에 따라 오역, 오정리가 있을 수 있으니, 관심이 있으시면 꼭 [원글](https://mattturck.com/mad2024/)을 참고해주세요.

_끝_