{
  "project": "Cooking Companion",
  "source_wbs": "Cooking_Companion_WBS.xlsx",
  "repository": "https://github.com/pop134/sample_PM_v6",
  "trunk": "main",
  "note": "Branch -> WBS requirement/task mapping. Kept OUTSIDE the git repository on purpose: the codebase must contain no WBS code or task ID. Each pull request delivers at most one task; every branch is based on the previous one so shared files never conflict, and all pull requests merge cumulatively toward main.",
  "phase": "Project code base plus requirements 1.1 through 1.6 (31 of 32 WBS tasks; requirement 1.7 QA/Testing/Deployment remains)",
  "requirements": {
    "1.1": "User Authentication & Profile Management",
    "1.2": "Recipe Management & Following",
    "1.3": "Photo Capture & Media Management",
    "1.4": "Cooking Sessions & Journal",
    "1.5": "Community Reviews & Ratings",
    "1.6": "Search, Feed & Social Discovery",
    "1.7": "QA, Testing & Deployment"
  },
  "branches": [
    {
      "pr": 1,
      "branch": "foundation",
      "base": "main",
      "wbs_code": null,
      "task": "Project code base (prerequisite for every WBS task)",
      "title": "Project foundation: application skeleton and shared core",
      "url": "https://github.com/pop134/sample_PM_v6/pull/1",
      "tests_passing": 17
    },
    {
      "pr": 2,
      "branch": "auth-data-models",
      "base": "foundation",
      "wbs_code": "1.1.1",
      "task": "[BE] Auth & user data models + DB schema",
      "title": "Account data models and database schema",
      "url": "https://github.com/pop134/sample_PM_v6/pull/2",
      "tests_passing": 28
    },
    {
      "pr": 3,
      "branch": "auth-registration-login",
      "base": "auth-data-models",
      "wbs_code": "1.1.2",
      "task": "[BE] Registration, login & password hashing",
      "title": "Registration, login and password hashing",
      "url": "https://github.com/pop134/sample_PM_v6/pull/3",
      "tests_passing": 38
    },
    {
      "pr": 4,
      "branch": "auth-sessions-middleware",
      "base": "auth-registration-login",
      "wbs_code": "1.1.3",
      "task": "[BE] Session/token management & auth middleware",
      "title": "Session token management and route protection",
      "url": "https://github.com/pop134/sample_PM_v6/pull/4",
      "tests_passing": 46
    },
    {
      "pr": 5,
      "branch": "profile-api",
      "base": "auth-sessions-middleware",
      "wbs_code": "1.1.4",
      "task": "[BE] Profile CRUD API",
      "title": "Profile read and update API",
      "url": "https://github.com/pop134/sample_PM_v6/pull/5",
      "tests_passing": 55
    },
    {
      "pr": 6,
      "branch": "auth-screens",
      "base": "profile-api",
      "wbs_code": "1.1.5",
      "task": "[FE] Registration & login screens",
      "title": "Registration and login screens",
      "url": "https://github.com/pop134/sample_PM_v6/pull/6",
      "tests_passing": 64
    },
    {
      "pr": 7,
      "branch": "profile-screens",
      "base": "auth-screens",
      "wbs_code": "1.1.6",
      "task": "[FE] Profile view/edit UI",
      "title": "Profile view and edit UI",
      "url": "https://github.com/pop134/sample_PM_v6/pull/7",
      "tests_passing": 71
    },
    {
      "pr": 8,
      "branch": "recipe-data-model",
      "base": "profile-screens",
      "wbs_code": "1.2.1",
      "task": "[BE] Recipe data model",
      "title": "Recipe data model",
      "url": "https://github.com/pop134/sample_PM_v6/pull/8",
      "tests_passing": 79
    },
    {
      "pr": 9,
      "branch": "recipe-crud-api",
      "base": "recipe-data-model",
      "wbs_code": "1.2.2",
      "task": "[BE] Recipe CRUD API",
      "title": "Recipe CRUD API",
      "url": "https://github.com/pop134/sample_PM_v6/pull/9",
      "tests_passing": 90
    },
    {
      "pr": 10,
      "branch": "ingredient-scaling",
      "base": "recipe-crud-api",
      "wbs_code": "1.2.3",
      "task": "[BE] Ingredient scaling & unit conversion",
      "title": "Ingredient scaling and unit conversion",
      "url": "https://github.com/pop134/sample_PM_v6/pull/10",
      "tests_passing": 101
    },
    {
      "pr": 11,
      "branch": "cook-mode-api",
      "base": "ingredient-scaling",
      "wbs_code": "1.2.4",
      "task": "[BE] Step-by-step cook-mode API",
      "title": "Step-by-step cook-mode API",
      "url": "https://github.com/pop134/sample_PM_v6/pull/11",
      "tests_passing": 111
    },
    {
      "pr": 12,
      "branch": "recipe-browse-ui",
      "base": "cook-mode-api",
      "wbs_code": "1.2.5",
      "task": "[FE] Recipe browse & detail screens",
      "title": "Recipe browse and detail screens",
      "url": "https://github.com/pop134/sample_PM_v6/pull/12",
      "tests_passing": 118
    },
    {
      "pr": 13,
      "branch": "recipe-form-ui",
      "base": "recipe-browse-ui",
      "wbs_code": "1.2.6",
      "task": "[FE] Recipe create/edit form UI",
      "title": "Recipe create and edit form UI",
      "url": "https://github.com/pop134/sample_PM_v6/pull/13",
      "tests_passing": 129
    },
    {
      "pr": 14,
      "branch": "guided-cooking-ui",
      "base": "recipe-form-ui",
      "wbs_code": "1.2.7",
      "task": "[FE] Guided cooking UI with timers",
      "title": "Guided cooking UI with timers",
      "url": "https://github.com/pop134/sample_PM_v6/pull/14",
      "tests_passing": 136
    },
    {
      "pr": 15,
      "branch": "media-storage",
      "base": "guided-cooking-ui",
      "wbs_code": "1.3.1",
      "task": "[BE] Media storage design",
      "title": "Media storage design",
      "url": "https://github.com/pop134/sample_PM_v6/pull/15",
      "tests_passing": 143
    },
    {
      "pr": 16,
      "branch": "media-upload-api",
      "base": "media-storage",
      "wbs_code": "1.3.2",
      "task": "[BE] Image upload/save API",
      "title": "Image upload and serving API",
      "url": "https://github.com/pop134/sample_PM_v6/pull/16",
      "tests_passing": 154
    },
    {
      "pr": 17,
      "branch": "thumbnail-generation",
      "base": "media-upload-api",
      "wbs_code": "1.3.3",
      "task": "[BE] Thumbnail generation & serving",
      "title": "Thumbnail generation and serving",
      "url": "https://github.com/pop134/sample_PM_v6/pull/17",
      "tests_passing": 161
    },
    {
      "pr": 18,
      "branch": "camera-capture-ui",
      "base": "thumbnail-generation",
      "wbs_code": "1.3.4",
      "task": "[FE] Camera capture (take picture)",
      "title": "In-app camera capture",
      "url": "https://github.com/pop134/sample_PM_v6/pull/18",
      "tests_passing": 168
    },
    {
      "pr": 19,
      "branch": "photo-gallery-ui",
      "base": "camera-capture-ui",
      "wbs_code": "1.3.5",
      "task": "[FE] Gallery / saved-pictures UI",
      "title": "Saved-pictures gallery UI",
      "url": "https://github.com/pop134/sample_PM_v6/pull/19",
      "tests_passing": 176
    },
    {
      "pr": 20,
      "branch": "attach-photos-ui",
      "base": "photo-gallery-ui",
      "wbs_code": "1.3.6",
      "task": "[FE] Attach photos to recipes/cooks UI",
      "title": "Attach photos to recipes UI",
      "url": "https://github.com/pop134/sample_PM_v6/pull/20",
      "tests_passing": 187
    },
    {
      "pr": 21,
      "branch": "cooking-session-model",
      "base": "attach-photos-ui",
      "wbs_code": "1.4.1",
      "task": "[BE] Cooking session model",
      "title": "Cooking session model",
      "url": "https://github.com/pop134/sample_PM_v6/pull/21",
      "tests_passing": 194
    },
    {
      "pr": 22,
      "branch": "session-logging-api",
      "base": "cooking-session-model",
      "wbs_code": "1.4.2",
      "task": "[BE] Session logging API",
      "title": "Cooking session logging API",
      "url": "https://github.com/pop134/sample_PM_v6/pull/22",
      "tests_passing": 206
    },
    {
      "pr": 23,
      "branch": "cook-log-ui",
      "base": "session-logging-api",
      "wbs_code": "1.4.3",
      "task": "[FE] Log-a-cook flow & history UI",
      "title": "Log-a-cook flow and history UI",
      "url": "https://github.com/pop134/sample_PM_v6/pull/23",
      "tests_passing": 216
    },
    {
      "pr": 24,
      "branch": "review-data-model",
      "base": "cook-log-ui",
      "wbs_code": "1.5.1",
      "task": "[BE] Review/rating data model",
      "title": "Review and rating data model",
      "url": "https://github.com/pop134/sample_PM_v6/pull/24",
      "tests_passing": 220
    },
    {
      "pr": 25,
      "branch": "review-crud-aggregation",
      "base": "review-data-model",
      "wbs_code": "1.5.2",
      "task": "[BE] Review CRUD & rating aggregation",
      "title": "Review CRUD and rating aggregation",
      "url": "https://github.com/pop134/sample_PM_v6/pull/25",
      "tests_passing": 234
    },
    {
      "pr": 26,
      "branch": "moderation-reporting",
      "base": "review-crud-aggregation",
      "wbs_code": "1.5.3",
      "task": "[BE] Moderation & abuse reporting",
      "title": "Abuse reporting and moderation queue",
      "url": "https://github.com/pop134/sample_PM_v6/pull/26",
      "tests_passing": 244
    },
    {
      "pr": 27,
      "branch": "public-cook-page",
      "base": "moderation-reporting",
      "wbs_code": "1.5.4",
      "task": "[FE] Cook detail page with reviews",
      "title": "Public cook page with ratings and reviews",
      "url": "https://github.com/pop134/sample_PM_v6/pull/27",
      "tests_passing": 251
    },
    {
      "pr": 28,
      "branch": "review-compose-ui",
      "base": "public-cook-page",
      "wbs_code": "1.5.5",
      "task": "[FE] Write-a-review & report UI",
      "title": "Write-a-review and report UI",
      "url": "https://github.com/pop134/sample_PM_v6/pull/28",
      "tests_passing": 265
    },
    {
      "pr": 29,
      "branch": "search-indexing",
      "base": "review-compose-ui",
      "wbs_code": "1.6.1",
      "task": "[BE] Search indexing",
      "title": "Search indexing for recipes, people and tags",
      "url": "https://github.com/pop134/sample_PM_v6/pull/29",
      "tests_passing": 286
    },
    {
      "pr": 30,
      "branch": "follow-feed-api",
      "base": "search-indexing",
      "wbs_code": "1.6.2",
      "task": "[BE] Follow relationships & feed API",
      "title": "Follow relationships and activity feed API",
      "url": "https://github.com/pop134/sample_PM_v6/pull/30",
      "tests_passing": 302
    },
    {
      "pr": 31,
      "branch": "feed-ranking",
      "base": "follow-feed-api",
      "wbs_code": "1.6.3",
      "task": "[BE] Feed ranking & pagination",
      "title": "Feed ranking and cursor pagination",
      "url": "https://github.com/pop134/sample_PM_v6/pull/31",
      "tests_passing": 324
    },
    {
      "pr": 32,
      "branch": "search-ui",
      "base": "feed-ranking",
      "wbs_code": "1.6.4",
      "task": "[FE] Search UI with filters",
      "title": "Search UI with kind and tag filters",
      "url": "https://github.com/pop134/sample_PM_v6/pull/32",
      "tests_passing": 338
    },
    {
      "pr": 33,
      "branch": "feed-discovery-ui",
      "base": "search-ui",
      "wbs_code": "1.6.5",
      "task": "[FE] Home feed & discovery UI",
      "title": "Home feed and discovery UI",
      "url": "https://github.com/pop134/sample_PM_v6/pull/33",
      "tests_passing": 355
    }
  ],
  "remaining_tasks": {
    "1.7.1": "[BE] Backend unit & integration tests",
    "1.7.2": "[FE] Frontend UI & end-to-end tests",
    "1.7.3": "[BE] Packaging, config & environment setup",
    "1.7.4": "[BE] CI/CD pipeline & release build",
    "1.7.5": "[FE] UAT, bug-fix pass & final polish"
  },
  "latest_branch": "feed-discovery-ui"
}


```
{
  "project": "Cooking Companion (pop134/sample_PM_v5)",
  "note": "Branch -> WBS requirement/task mapping. Kept OUTSIDE the git repo on purpose: the codebase must contain no WBS/Task ID traces. Each PR = at most one task; tasks are split across >=2 stacked PRs, each branch based on the previous so shared files never conflict. All PRs merge cumulatively toward main.",
  "trunk": "main",
  "requirements": {
    "1.1": "User Authentication & Profile Management",
    "1.2": "Recipe Management & Following",
    "1.3": "Photo Capture & Media Management",
    "1.4": "Cooking Sessions & Journal",
    "1.5": "Community Reviews & Ratings",
    "1.6": "Search, Feed & Social Discovery",
    "1.7": "QA, Testing & Deployment"
  },
  "tasks": {
    "1.1.1": "[BE] Auth & user data models + DB schema",
    "1.1.2": "[BE] Registration, login & password hashing",
    "1.1.3": "[BE] Session/token management & auth middleware",
    "1.1.4": "[BE] Profile CRUD API",
    "1.1.5": "[FE] Registration & login screens",
    "1.1.6": "[FE] Profile view/edit UI",
    "1.2.1": "[BE] Recipe data model",
    "1.2.2": "[BE] Recipe CRUD API",
    "1.2.3": "[BE] Ingredient scaling & unit conversion",
    "1.2.4": "[BE] Step-by-step cook-mode API",
    "1.2.5": "[FE] Recipe browse & detail screens",
    "1.2.6": "[FE] Recipe create/edit form UI",
    "1.2.7": "[FE] Guided cooking UI with timers",
    "1.3.1": "[BE] Media storage design",
    "1.3.2": "[BE] Image upload/save API",
    "1.3.3": "[BE] Thumbnail generation & serving",
    "1.3.4": "[FE] Camera capture (take picture)",
    "1.3.5": "[FE] Gallery / saved-pictures UI",
    "1.3.6": "[FE] Attach photos to recipes/cooks UI",
    "1.4.1": "[BE] Cooking session model",
    "1.4.2": "[BE] Session logging API",
    "1.4.3": "[FE] Log-a-cook flow & history UI",
    "1.5.1": "[BE] Review/rating data model",
    "1.5.2": "[BE] Review CRUD & rating aggregation",
    "1.5.3": "[BE] Moderation & abuse reporting",
    "1.5.4": "[FE] Cook detail page with reviews",
    "1.5.5": "[FE] Write-a-review & report UI",
    "1.6.1": "[BE] Search indexing",
    "1.6.2": "[BE] Follow relationships & feed API",
    "1.6.3": "[BE] Feed ranking & pagination",
    "1.6.4": "[FE] Search UI with filters",
    "1.6.5": "[FE] Home feed & discovery UI",
    "1.7.1": "[BE] Backend unit & integration tests",
    "1.7.2": "[FE] Frontend UI & end-to-end tests",
    "1.7.3": "[BE] Packaging, config & environment setup",
    "1.7.4": "[BE] CI/CD pipeline & release build",
    "1.7.5": "[FE] UAT, bug-fix pass & final polish"
  },
  "branches": [
    {
      "pr": 1,
      "branch": "foundation",
      "base": "main",
      "requirement": null,
      "task": null,
      "part": null,
      "title": "Foundation: full-Python application skeleton"
    },
    {
      "pr": 2,
      "branch": "models-part-1",
      "base": "foundation",
      "requirement": "1.1",
      "task": "1.1.1",
      "part": "1/2",
      "title": "Account & profile data models"
    },
    {
      "pr": 3,
      "branch": "models-part-2",
      "base": "models-part-1",
      "requirement": "1.1",
      "task": "1.1.1",
      "part": "2/2",
      "title": "Session model & repository layer"
    },
    {
      "pr": 4,
      "branch": "auth-register-part-1",
      "base": "models-part-2",
      "requirement": "1.1",
      "task": "1.1.2",
      "part": "1/2",
      "title": "Account registration"
    },
    {
      "pr": 5,
      "branch": "auth-login-part-2",
      "base": "auth-register-part-1",
      "requirement": "1.1",
      "task": "1.1.2",
      "part": "2/2",
      "title": "Login & session issuance"
    },
    {
      "pr": 6,
      "branch": "auth-middleware-part-1",
      "base": "auth-login-part-2",
      "requirement": "1.1",
      "task": "1.1.3",
      "part": "1/2",
      "title": "Session resolution & auth dependencies"
    },
    {
      "pr": 7,
      "branch": "auth-sessions-part-2",
      "base": "auth-middleware-part-1",
      "requirement": "1.1",
      "task": "1.1.3",
      "part": "2/2",
      "title": "Session lifecycle management"
    },
    {
      "pr": 8,
      "branch": "profile-crud-part-1",
      "base": "auth-sessions-part-2",
      "requirement": "1.1",
      "task": "1.1.4",
      "part": "1/2",
      "title": "Profile read API & preferences"
    },
    {
      "pr": 9,
      "branch": "profile-crud-part-2",
      "base": "profile-crud-part-1",
      "requirement": "1.1",
      "task": "1.1.4",
      "part": "2/2",
      "title": "Profile update endpoint"
    },
    {
      "pr": 10,
      "branch": "auth-ui-register-part-1",
      "base": "profile-crud-part-2",
      "requirement": "1.1",
      "task": "1.1.5",
      "part": "1/2",
      "title": "Registration screen"
    },
    {
      "pr": 11,
      "branch": "auth-ui-login-part-2",
      "base": "auth-ui-register-part-1",
      "requirement": "1.1",
      "task": "1.1.5",
      "part": "2/2",
      "title": "Login screen & logout"
    },
    {
      "pr": 12,
      "branch": "profile-ui-view-part-1",
      "base": "auth-ui-login-part-2",
      "requirement": "1.1",
      "task": "1.1.6",
      "part": "1/2",
      "title": "Profile view page"
    },
    {
      "pr": 13,
      "branch": "profile-ui-edit-part-2",
      "base": "profile-ui-view-part-1",
      "requirement": "1.1",
      "task": "1.1.6",
      "part": "2/2",
      "title": "Profile edit form"
    },
    {
      "pr": 14,
      "branch": "recipe-model-part-1",
      "base": "profile-ui-edit-part-2",
      "requirement": "1.2",
      "task": "1.2.1",
      "part": "1/2",
      "title": "Recipe & ingredient models"
    },
    {
      "pr": 15,
      "branch": "recipe-model-part-2",
      "base": "recipe-model-part-1",
      "requirement": "1.2",
      "task": "1.2.1",
      "part": "2/2",
      "title": "Recipe steps, tags & repository"
    },
    {
      "pr": 16,
      "branch": "recipe-crud-part-1",
      "base": "recipe-model-part-2",
      "requirement": "1.2",
      "task": "1.2.2",
      "part": "1/2",
      "title": "Recipe create / read / list API"
    },
    {
      "pr": 17,
      "branch": "recipe-crud-part-2",
      "base": "recipe-crud-part-1",
      "requirement": "1.2",
      "task": "1.2.2",
      "part": "2/2",
      "title": "Recipe update & delete"
    },
    {
      "pr": 18,
      "branch": "recipe-units-part-1",
      "base": "recipe-crud-part-2",
      "requirement": "1.2",
      "task": "1.2.3",
      "part": "1/2",
      "title": "Unit conversion module"
    },
    {
      "pr": 19,
      "branch": "recipe-scaling-part-2",
      "base": "recipe-units-part-1",
      "requirement": "1.2",
      "task": "1.2.3",
      "part": "2/2",
      "title": "Ingredient scaling endpoint"
    },
    {
      "pr": 20,
      "branch": "cookmode-part-1",
      "base": "recipe-scaling-part-2",
      "requirement": "1.2",
      "task": "1.2.4",
      "part": "1/2",
      "title": "Cook-mode steps & start"
    },
    {
      "pr": 21,
      "branch": "cookmode-part-2",
      "base": "cookmode-part-1",
      "requirement": "1.2",
      "task": "1.2.4",
      "part": "2/2",
      "title": "Cook-mode progress"
    },
    {
      "pr": 22,
      "branch": "recipe-ui-browse-part-1",
      "base": "cookmode-part-2",
      "requirement": "1.2",
      "task": "1.2.5",
      "part": "1/2",
      "title": "Recipe browse page"
    },
    {
      "pr": 23,
      "branch": "recipe-ui-detail-part-2",
      "base": "recipe-ui-browse-part-1",
      "requirement": "1.2",
      "task": "1.2.5",
      "part": "2/2",
      "title": "Recipe detail page"
    },
    {
      "pr": 24,
      "branch": "recipe-ui-create-part-1",
      "base": "recipe-ui-detail-part-2",
      "requirement": "1.2",
      "task": "1.2.6",
      "part": "1/2",
      "title": "Recipe create form"
    },
    {
      "pr": 25,
      "branch": "recipe-ui-edit-part-2",
      "base": "recipe-ui-create-part-1",
      "requirement": "1.2",
      "task": "1.2.6",
      "part": "2/2",
      "title": "Recipe edit form"
    },
    {
      "pr": 26,
      "branch": "cook-ui-steps-part-1",
      "base": "recipe-ui-edit-part-2",
      "requirement": "1.2",
      "task": "1.2.7",
      "part": "1/2",
      "title": "Guided cooking step view"
    },
    {
      "pr": 27,
      "branch": "cook-ui-timer-part-2",
      "base": "cook-ui-steps-part-1",
      "requirement": "1.2",
      "task": "1.2.7",
      "part": "2/2",
      "title": "Guided cooking countdown timer"
    },
    {
      "pr": 28,
      "branch": "media-model-part-1",
      "base": "cook-ui-timer-part-2",
      "requirement": "1.3",
      "task": "1.3.1",
      "part": "1/2",
      "title": "Media asset model & repository"
    },
    {
      "pr": 29,
      "branch": "media-storage-part-2",
      "base": "media-model-part-1",
      "requirement": "1.3",
      "task": "1.3.1",
      "part": "2/2",
      "title": "Filesystem media store & config"
    },
    {
      "pr": 30,
      "branch": "media-upload-part-1",
      "base": "media-storage-part-2",
      "requirement": "1.3",
      "task": "1.3.2",
      "part": "1/2",
      "title": "Image upload endpoint"
    },
    {
      "pr": 31,
      "branch": "media-serve-part-2",
      "base": "media-upload-part-1",
      "requirement": "1.3",
      "task": "1.3.2",
      "part": "2/2",
      "title": "Media fetch, list, delete & raw serving"
    },
    {
      "pr": 32,
      "branch": "media-thumb-gen-part-1",
      "base": "media-serve-part-2",
      "requirement": "1.3",
      "task": "1.3.3",
      "part": "1/2",
      "title": "Thumbnail generation"
    },
    {
      "pr": 33,
      "branch": "media-thumb-serve-part-2",
      "base": "media-thumb-gen-part-1",
      "requirement": "1.3",
      "task": "1.3.3",
      "part": "2/2",
      "title": "Thumbnail serving"
    },
    {
      "pr": 34,
      "branch": "photo-ui-upload-part-1",
      "base": "media-thumb-serve-part-2",
      "requirement": "1.3",
      "task": "1.3.4",
      "part": "1/2",
      "title": "Photo upload page"
    },
    {
      "pr": 35,
      "branch": "photo-ui-capture-part-2",
      "base": "photo-ui-upload-part-1",
      "requirement": "1.3",
      "task": "1.3.4",
      "part": "2/2",
      "title": "In-app camera capture"
    },
    {
      "pr": 36,
      "branch": "photo-ui-gallery-part-1",
      "base": "photo-ui-capture-part-2",
      "requirement": "1.3",
      "task": "1.3.5",
      "part": "1/2",
      "title": "Photo gallery grid"
    },
    {
      "pr": 37,
      "branch": "photo-ui-view-part-2",
      "base": "photo-ui-gallery-part-1",
      "requirement": "1.3",
      "task": "1.3.5",
      "part": "2/2",
      "title": "Photo detail view & delete"
    },
    {
      "pr": 38,
      "branch": "recipe-photos-attach-part-1",
      "base": "photo-ui-view-part-2",
      "requirement": "1.3",
      "task": "1.3.6",
      "part": "1/2",
      "title": "Attach photos to recipes"
    },
    {
      "pr": 39,
      "branch": "recipe-photos-show-part-2",
      "base": "recipe-photos-attach-part-1",
      "requirement": "1.3",
      "task": "1.3.6",
      "part": "2/2",
      "title": "Show recipe photos & detach"
    },
    {
      "pr": 40,
      "branch": "cooklog-model-part-1",
      "base": "recipe-photos-show-part-2",
      "requirement": "1.4",
      "task": "1.4.1",
      "part": "1/2",
      "title": "Cooking journal model"
    },
    {
      "pr": 41,
      "branch": "cooklog-photos-part-2",
      "base": "cooklog-model-part-1",
      "requirement": "1.4",
      "task": "1.4.1",
      "part": "2/2",
      "title": "Cook log photo attachments"
    },
    {
      "pr": 42,
      "branch": "cook-log-api-part-1",
      "base": "cooklog-photos-part-2",
      "requirement": "1.4",
      "task": "1.4.2",
      "part": "1/2",
      "title": "Cooking session logging API"
    },
    {
      "pr": 43,
      "branch": "cook-log-photos-api-part-2",
      "base": "cook-log-api-part-1",
      "requirement": "1.4",
      "task": "1.4.2",
      "part": "2/2",
      "title": "Cook photo attachment API"
    },
    {
      "pr": 44,
      "branch": "cook-ui-log-part-1",
      "base": "cook-log-photos-api-part-2",
      "requirement": "1.4",
      "task": "1.4.3",
      "part": "1/2",
      "title": "Log-a-cook flow & history"
    },
    {
      "pr": 45,
      "branch": "cook-ui-detail-part-2",
      "base": "cook-ui-log-part-1",
      "requirement": "1.4",
      "task": "1.4.3",
      "part": "2/2",
      "title": "Cook editing & photo attachment UI"
    },
    {
      "pr": 46,
      "branch": "review-model-part-1",
      "base": "cook-ui-detail-part-2",
      "requirement": "1.5",
      "task": "1.5.1",
      "part": "1/2",
      "title": "Review data model"
    },
    {
      "pr": 47,
      "branch": "review-aggregation-part-2",
      "base": "review-model-part-1",
      "requirement": "1.5",
      "task": "1.5.1",
      "part": "2/2",
      "title": "Rating aggregation queries"
    },
    {
      "pr": 48,
      "branch": "review-crud-part-1",
      "base": "review-aggregation-part-2",
      "requirement": "1.5",
      "task": "1.5.2",
      "part": "1/2",
      "title": "Review create/update/delete API"
    },
    {
      "pr": 49,
      "branch": "review-list-part-2",
      "base": "review-crud-part-1",
      "requirement": "1.5",
      "task": "1.5.2",
      "part": "2/2",
      "title": "Review listing & rating summary API"
    },
    {
      "pr": 50,
      "branch": "report-model-part-1",
      "base": "review-list-part-2",
      "requirement": "1.5",
      "task": "1.5.3",
      "part": "1/2",
      "title": "Abuse report model & reporting"
    },
    {
      "pr": 51,
      "branch": "moderation-queue-part-2",
      "base": "report-model-part-1",
      "requirement": "1.5",
      "task": "1.5.3",
      "part": "2/2",
      "title": "Moderation queue & review hiding"
    },
    {
      "pr": 52,
      "branch": "cook-public-page-part-1",
      "base": "moderation-queue-part-2",
      "requirement": "1.5",
      "task": "1.5.4",
      "part": "1/2",
      "title": "Public cook page with rating"
    },
    {
      "pr": 53,
      "branch": "cook-reviews-list-part-2",
      "base": "cook-public-page-part-1",
      "requirement": "1.5",
      "task": "1.5.4",
      "part": "2/2",
      "title": "Reviews on the public cook page"
    },
    {
      "pr": 54,
      "branch": "write-review-ui-part-1",
      "base": "cook-reviews-list-part-2",
      "requirement": "1.5",
      "task": "1.5.5",
      "part": "1/2",
      "title": "Write-a-review UI"
    },
    {
      "pr": 55,
      "branch": "report-review-ui-part-2",
      "base": "write-review-ui-part-1",
      "requirement": "1.5",
      "task": "1.5.5",
      "part": "2/2",
      "title": "Report control on reviews"
    },
    {
      "pr": 56,
      "branch": "search-recipes-part-1",
      "base": "report-review-ui-part-2",
      "requirement": "1.6",
      "task": "1.6.1",
      "part": "1/2",
      "title": "Recipe search"
    },
    {
      "pr": 57,
      "branch": "search-users-part-2",
      "base": "search-recipes-part-1",
      "requirement": "1.6",
      "task": "1.6.1",
      "part": "2/2",
      "title": "User search"
    },
    {
      "pr": 58,
      "branch": "follow-model-part-1",
      "base": "search-users-part-2",
      "requirement": "1.6",
      "task": "1.6.2",
      "part": "1/2",
      "title": "Follow relationships"
    },
    {
      "pr": 59,
      "branch": "feed-api-part-2",
      "base": "follow-model-part-1",
      "requirement": "1.6",
      "task": "1.6.2",
      "part": "2/2",
      "title": "Activity feed API"
    },
    {
      "pr": 60,
      "branch": "feed-ranking-part-1",
      "base": "feed-api-part-2",
      "requirement": "1.6",
      "task": "1.6.3",
      "part": "1/2",
      "title": "Feed ranking"
    },
    {
      "pr": 61,
      "branch": "feed-discovery-part-2",
      "base": "feed-ranking-part-1",
      "requirement": "1.6",
      "task": "1.6.3",
      "part": "2/2",
      "title": "Discovery feed"
    },
    {
      "pr": 62,
      "branch": "search-ui-recipes-part-1",
      "base": "feed-discovery-part-2",
      "requirement": "1.6",
      "task": "1.6.4",
      "part": "1/2",
      "title": "Search page with recipe results"
    },
    {
      "pr": 63,
      "branch": "search-ui-people-part-2",
      "base": "search-ui-recipes-part-1",
      "requirement": "1.6",
      "task": "1.6.4",
      "part": "2/2",
      "title": "People results & type filter"
    },
    {
      "pr": 64,
      "branch": "feed-ui-home-part-1",
      "base": "search-ui-people-part-2",
      "requirement": "1.6",
      "task": "1.6.5",
      "part": "1/2",
      "title": "Home feed page"
    },
    {
      "pr": 65,
      "branch": "discovery-ui-part-2",
      "base": "feed-ui-home-part-1",
      "requirement": "1.6",
      "task": "1.6.5",
      "part": "2/2",
      "title": "Discovery & public user profiles"
    },
    {
      "pr": 66,
      "branch": "backend-integration-tests-part-1",
      "base": "discovery-ui-part-2",
      "requirement": "1.7",
      "task": "1.7.1",
      "part": "1/2",
      "title": "Backend integration journey tests"
    },
    {
      "pr": 67,
      "branch": "backend-edge-tests-part-2",
      "base": "backend-integration-tests-part-1",
      "requirement": "1.7",
      "task": "1.7.1",
      "part": "2/2",
      "title": "Backend edge-case & regression tests"
    },
    {
      "pr": 68,
      "branch": "web-e2e-tests-part-1",
      "base": "backend-edge-tests-part-2",
      "requirement": "1.7",
      "task": "1.7.2",
      "part": "1/2",
      "title": "End-to-end web journey tests"
    },
    {
      "pr": 69,
      "branch": "web-ui-tests-part-2",
      "base": "web-e2e-tests-part-1",
      "requirement": "1.7",
      "task": "1.7.2",
      "part": "2/2",
      "title": "UI navigation, error-page & validation tests"
    },
    {
      "pr": 70,
      "branch": "packaging-part-1",
      "base": "web-ui-tests-part-2",
      "requirement": "1.7",
      "task": "1.7.3",
      "part": "1/2",
      "title": "Container packaging & production server"
    },
    {
      "pr": 71,
      "branch": "config-guard-part-2",
      "base": "packaging-part-1",
      "requirement": "1.7",
      "task": "1.7.3",
      "part": "2/2",
      "title": "Production config guard & Makefile"
    },
    {
      "pr": 72,
      "branch": "ci-enhance-part-1",
      "base": "config-guard-part-2",
      "requirement": "1.7",
      "task": "1.7.4",
      "part": "1/2",
      "title": "CI pipeline: lint, coverage & image build"
    },
    {
      "pr": 73,
      "branch": "release-workflow-part-2",
      "base": "ci-enhance-part-1",
      "requirement": "1.7",
      "task": "1.7.4",
      "part": "2/2",
      "title": "Tagged release build"
    },
    {
      "pr": 74,
      "branch": "polish-part-1",
      "base": "release-workflow-part-2",
      "requirement": "1.7",
      "task": "1.7.5",
      "part": "1/2",
      "title": "UAT polish: friendly 404 & accessibility"
    },
    {
      "pr": 75,
      "branch": "final-polish-part-2",
      "base": "polish-part-1",
      "requirement": "1.7",
      "task": "1.7.5",
      "part": "2/2",
      "title": "Final polish: favicon, About page & footer"
    }
  ],
  "status": "COMPLETE \u2014 all 7 requirements (1.1\u20131.7), 75 PRs, stacked, all CI green"
}
```
