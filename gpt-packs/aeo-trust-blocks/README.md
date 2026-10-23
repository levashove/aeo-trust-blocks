# aeo-trust-blocks — версия для ChatGPT (Custom GPT)

Тот же скилл, что `dist/claude-skills/aeo-trust-blocks/`, переупакованный под механику
ChatGPT: маршрутизатор — в поле Instructions, справочники — файлами в
Knowledge (retrieval). Папка производная, собрана `make skills-export`;
источники правды те же, что у скилла claude.ai (см. README скилла).

## Как собрать Custom GPT

1. [chatgpt.com](https://chatgpt.com) → My GPTs → **Create a GPT** →
   вкладка **Configure**.
2. **Name** — например, «aeo-trust-blocks». **Description** — можно взять первое
   предложение описания ниже.
3. **Instructions** — вставьте содержимое `instructions.txt` целиком
   (4173 символов из ~8000 лимита).
4. **Knowledge** — загрузите все файлы из `knowledge/`:
- `knowledge/aeo-methodology.md`
5. Сохраните (Only me — для личного использования).

Альтернатива без Custom GPT: Project в ChatGPT — те же instructions + файлы.

## Отличия от claude.ai-версии

- GPT не подхватывается автоматически по теме запроса — его нужно открыть.
- Knowledge работает через поиск по фрагментам (retrieval), а не чтение файла
  целиком: критичный минимум продублирован в Instructions, но детали
  справочников могут подтягиваться выборочно — при сомнении попросите GPT
  свериться с конкретным файлом.

## Описание скилла

AEO (Answer Engine Optimization): как попасть в ответы ChatGPT, Perplexity и Google AI Overviews. Аудит cite-safety готового текста по шкале 0–10 и переработка слабых участков в самодостаточные блоки — Extractable Trust Blocks, которые AI-поиск может безопасно извлекать и цитировать. Внутри: чек-лист самодостаточности, шесть типов Trust Blocks с формулой, шкала Cite-Safety Score, безопасная JSON-LD-разметка, контракт с голосом канала. Использовать при запросе оптимизировать текст для AI-выдачи, проверить цитируемость в AI-поисковиках или сделать AEO-аудит.
