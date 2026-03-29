# Оркестратор "Матрёшка" — полный цикл рецензирования

## Назначение
Выполнить полное рецензирование научной статьи по методологии "Матрёшка": от фильтрации тривиальности до синтеза итоговой рецензии.

## Входные данные
- Полный текст статьи (предоставляется пользователем)

## Ссылки на промпты

| Промпт | Ссылка |
|--------|--------|
| Глобальный | https://raw.githubusercontent.com/Famimot/ai-peer-review-prompt/main/prompt_en.md |
| Тривиальность | https://raw.githubusercontent.com/Famimot/ai-peer-review-prompt/main/subprompts/triviality_analyzer.md |
| Заголовок | https://raw.githubusercontent.com/Famimot/ai-peer-review-prompt/main/subprompts/title_analyzer.md |
| Аннотация | https://raw.githubusercontent.com/Famimot/ai-peer-review-prompt/main/subprompts/abstract_analyzer.md |
| Введение | https://raw.githubusercontent.com/Famimot/ai-peer-review-prompt/main/subprompts/introduction_analyzer.md |
| Методология | https://raw.githubusercontent.com/Famimot/ai-peer-review-prompt/main/subprompts/methodology_analyzer.md |
| Результаты | https://raw.githubusercontent.com/Famimot/ai-peer-review-prompt/main/subprompts/results_analyzer.md |
| Заключение | https://raw.githubusercontent.com/Famimot/ai-peer-review-prompt/main/subprompts/conclusion_analyzer.md |
| Литература | https://raw.githubusercontent.com/Famimot/ai-peer-review-prompt/main/subprompts/references_analyzer.md |
| Синтез | https://raw.githubusercontent.com/Famimot/ai-peer-review-prompt/main/subprompts/synthesis_analyzer.md |

## Алгоритм выполнения

### Шаг 1. Фильтр тривиальности
1. Загрузить содержимое промпта по ссылке "Тривиальность"
2. Выполнить анализ статьи по этому промпту
3. **Если балл тривиальности > 50** → сформировать заключение об отклонении (Вариант А) и завершить работу
4. **Если балл тривиальности ≤ 50** → продолжить

### Шаг 2. Глобальный анализ
1. Загрузить содержимое промпта по ссылке "Глобальный"
2. Выполнить анализ статьи

### Шаг 3. Пофрагментный анализ
Последовательно выполнить анализ по каждому узкому промпту в указанном порядке:
1. Заголовок
2. Аннотация
3. Введение
4. Методология
5. Результаты
6. Заключение
7. Литература

Для каждого:
- Загрузить содержимое промпта по соответствующей ссылке
- Выполнить анализ соответствующего фрагмента статьи

### Шаг 4. Синтез сводной рецензии
1. Загрузить содержимое промпта по ссылке "Синтез"
2. На основе всех накопленных результатов сформировать итоговую рецензию
3. Добавить обязательную фразу о соответствии ГОСТ

## Формат итогового вывода

### Вариант А: Статья отклонена на этапе тривиальности

```markdown
# Результат скрининга: Отклонено

**Балл тривиальности:** ___ из 100
**Уровень:** [Формальная / Тривиальная]

**Причины:**
- [причина 1]
- [причина 2]

**Рекомендация:** Статья не рекомендуется к дальнейшему рецензированию.
