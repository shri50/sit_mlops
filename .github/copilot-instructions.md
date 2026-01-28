# AI Coding Agent Instructions for MLOps Project

## Project Overview
This is an early-stage MLOps learning project focused on machine learning operations and hyperparameter management. The codebase is minimal but designed to grow with ML pipeline components.

## Current Architecture
- **main.py**: Entry point containing hyperparameter definitions and configuration
  - Currently stores hyperparameters in dictionary format (e.g., `learning_rate`)
  - Expected to expand with model training, data processing, and experiment tracking

## Key Patterns & Conventions

### Hyperparameter Management
- Store hyperparameters in dictionaries with clear naming: `hyp = {parameter_name: value}`
- Example: `learning_rate=0.33` (note: spacing inconsistency should be fixed - use `learning_rate = 0.33`)
- Future: Consider moving to config files (YAML/JSON) for experimentation tracking

### Code Style
- Use Python 3.x conventions
- Include debug/informational prints for pipeline stages
- **Known Issue**: Fix dictionary formatting in main.py (line 4 should separate dictionary into multiple lines for readability)

## Development Workflow
- No build system configured yet
- Run experiments: `python main.py`
- Expected additions: pytest for testing, data loading utilities, model training functions

## Integration Points (To Be Implemented)
- Data loading and preprocessing
- Model training loops
- Experiment tracking/logging
- Hyperparameter tuning frameworks

## Common Tasks
- **Adding new hyperparameters**: Extend the `hyp` dictionary in main.py
- **Implementing new ML stages**: Create separate modules (e.g., `data.py`, `train.py`, `model.py`) and import from main.py
- **Testing hyperparameters**: Run main.py and verify parameter values are correctly loaded

## Next Steps for AI Agents
When extending this project:
1. Maintain clear separation between configuration and logic
2. Add type hints for hyperparameters (consider using dataclasses or Pydantic)
3. Implement logging instead of print statements for production readiness
4. Add unit tests for hyperparameter loading and model initialization
