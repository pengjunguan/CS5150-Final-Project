# CLAUDE_TASK.md

## Current phase
Codebase migration diagnosis

---

## Background
- A large amount of code was copied from another Unreal Engine project
- Some renaming and adaptation have already been done
- However, the project is currently unstable and may contain hidden issues

---

## Primary objective
Inspect the current codebase and identify all problems caused by:

- incomplete migration
- incorrect renaming
- broken references
- Unreal-specific setup issues

---

## Key tasks

### 1. Project structure analysis
- Identify main modules
- Locate entry points
- Understand AI-related classes

---

### 2. Migration issue detection
Focus on:

- Old project names still present
- Module name mismatches
- Incorrect API macros (XXX_API)
- Broken include paths
- Missing or mismatched generated headers (.generated.h)
- Build.cs / Target.cs inconsistencies

---

### 3. Unreal-specific validation
- Check UObject / Actor declarations
- Validate UCLASS / UPROPERTY / UFUNCTION usage
- Check AIController, BehaviorTree, Blackboard integration

---

### 4. Logic consistency check
- Compare current code with intended AI design:
  - Easy / Medium / Hard modes
- Identify missing or inconsistent behaviors

---

## Output requirements
When reporting findings:

- List issues in a structured way
- For each issue:
  - File location
  - Problem description
  - Why it is problematic
  - Suggested minimal fix

---

## Constraints
- DO NOT implement new features yet
- DO NOT refactor large portions of code
- Focus only on diagnosis and small fixes

---

## Next phase (future)
After stabilization:

- Implement AI behavior system:
  - Behavior Tree design
  - Awareness system
  - Communication between AI
  - Cover system
  - Regeneration logic
