# Enable a new GitHub Copilot model

This skill creates a PR to enable a new model in the enterprise-level Copilot settings.

## Usage

Provide the full model name (e.g. "Anthropic Claude Opus 4.7", "OpenAI GPT-5.5", "Google Gemini 4 Pro").

## Steps

1. Read the current state of `docs/decisions/0002-enterprise-ai-controls.md`.
2. Checkout a new branch from `main` named `enable-<model-name-lowercased-with-hyphens>` (e.g. `enable-claude-opus-4.7`, `enable-gpt-5.5`). The model vendor prefix (e.g. "Anthropic", "OpenAI", "Google") should be **excluded** from the branch name.
3. Make three changes to `docs/decisions/0002-enterprise-ai-controls.md`:
   - **Update "Last Updated" date** on line 4 to today's date in `YYYY-MM-DD` format.
  - **Add a new row** to the `### Default models` table for the new model. Insert it in the correct position among its vendor group (Anthropic, Google, OpenAI, xAI), maintaining alphabetical/version order within that group. Use `Optional` for the `Status` value. Pad with spaces to align the table columns.
   - **Add an amendments entry** at the bottom of the `## Amendments` section using this format:
     ```
     ### DD/MM/YY ([source](https://github.com/ministryofjustice/.github/pull/PLACEHOLDER))

     - Enable <Model Display Name>
     ```
     Use today's date in `DD/MM/YY` format. Use `PLACEHOLDER` for the PR number initially.
4. Commit the changes with the message `:copilot: Enable <Model Display Name>`.
5. Push the branch to origin.
6. Create a PR with:
   - **Title:** `:copilot: Enable <Model Display Name>`
   - **Body:**
     ```
     ## Proposed Changes

     - Enables <Model Display Name> model
     ```
   - **Base:** `main`
7. After the PR is created and you have the PR number, update the `PLACEHOLDER` in the amendments section with the actual PR number, commit with message `Update PR number reference`, and push again.

## Example

For model name "Anthropic Claude Opus 4.7":

- **Branch:** `enable-claude-opus-4.7`
- **PR Title:** `:copilot: Enable Claude Opus 4.7`
- **PR Body:**
  ```
  ## Proposed Changes

  - Enables Claude Opus 4.7 model
  ```
- **Table row:** `| Anthropic Claude Opus 4.7                       | Optional |`
- **Amendment:** `### 16/04/26 ([source](https://github.com/ministryofjustice/.github/pull/40))\n\n- Enable Claude Opus 4.7`

## Important Notes

- The model display name in the PR title, body, commit message, and amendments should **not** include the vendor prefix (e.g. use "Claude Opus 4.7" not "Anthropic Claude Opus 4.7"). The vendor prefix is only used in the models table row.
- The branch name uses the model name without the vendor prefix, lowercased, with spaces replaced by hyphens.
- Always check the current state of the file first to avoid duplicates and to find the correct insertion point.
