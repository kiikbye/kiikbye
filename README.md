<h1 align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&amp;height=155&amp;color=0:0d1117,100:162e4d&amp;text=Merei%20Kiikbayev&amp;fontSize=54&amp;fontColor=e6edf3&amp;fontAlignY=39&amp;animation=fadeIn" alt="Merei Kiikbayev" width="100%">
</h1>
<p align="center"><strong>Computer Science Student</strong> · Backend Development · Distributed Systems</p>

## Featured Project

### [TaskFlow · Distributed Job Processing](https://github.com/kiikbye/taskflow)

**Published prototype** · [Dashboard screenshot](https://github.com/kiikbye/taskflow/blob/main/evidence/parallel-dashboard.png)

TaskFlow splits a batch into independent jobs and distributes them to Celery workers. The dashboard shows which worker handled each job, how long it took, and whether it needed a retry. If a worker stops mid-job, the dispatcher can requeue the unfinished work after its execution window expires.

```mermaid
flowchart LR
    Web["Django dashboard and API"] -->|Save jobs| DB[(PostgreSQL)]
    DB -->|Pending jobs| Dispatcher[Dispatcher]
    Dispatcher -->|Publish| Broker[RabbitMQ]
    Broker -->|Deliver| Workers[Celery workers]
    Workers -->|Record attempts and results| DB
    classDef primary fill:#152d4a,stroke:#58a6ff,color:#eff6ff
    class Web,Workers primary
```

**Recorded demo** · The same nine jobs with simulated wait time took **18.42 s on one worker** and **6.27 s on three**. The two runs returned the same result. In a separate failure test, another worker completed a job after the original worker stopped.

`Python` · `Django REST Framework` · `PostgreSQL` · `RabbitMQ` · `Celery` · `Redis` · `Docker Compose`

## More Projects

| Project | What it demonstrates | Status |
| --- | --- | --- |
| **Sokoban** | A retro C++ puzzle game with three levels, undo, move tracking, and a custom SDL2/OpenGL renderer. | [View repository](https://github.com/kiikbye/sokoban) |
| **Kazakh–Russian LLM Evaluation** | A reproducible Python benchmark for software issue routing. Compared zero-shot and few-shot prompts on 30 held-out issues and published raw model responses and per-language scores. | [View repository](https://github.com/kiikbye/kk-ru-llm-eval) · [Results](https://github.com/kiikbye/kk-ru-llm-eval/blob/main/results/report.md) |
| **ResilientQ** | A Redis-backed job queue with a FastAPI service, expiring job leases, retries, and a worker failure experiment. | Local prototype |
| **Shift Planner** | A mobile calendar prototype for a repeating day, night, and rest schedule. | Prototype |
| **Room Plant Classifier** | A Jupyter notebook comparing a custom CNN with MobileNetV2 transfer learning for image classification. | Coursework notebook |
| **Computer Graphics Labs** | C++17 and OpenGL exercises covering shaders, indexed drawing, 3D transforms, and a free camera. | [View repository](https://github.com/kiikbye/-computer-grafica) |

## About Me

I'm a Computer Science student at Al-Farabi Kazakh National University. I enjoy building tools that solve practical problems and testing what happens when part of a system fails. My coursework also includes computer graphics and image classification.

## Tech Stack

![Python, C++, Django, FastAPI, PostgreSQL, Redis, React, Docker, and Git](https://skillicons.dev/icons?i=python,cpp,django,fastapi,postgres,redis,react,docker,git&theme=dark)

**Languages** · Python, C++, JavaScript, HTML, CSS  
**Backend and data** · Django, Django REST Framework, FastAPI, PostgreSQL, Redis, RabbitMQ, Celery  
**Frontend and graphics** · React, OpenGL, SDL2, GLFW, GLM  
**Tooling** · Docker Compose, Git, CMake, Jupyter

## GitHub Activity

[![GitHub contribution streak for kiikbye](https://streak-stats.demolab.com?user=kiikbye&theme=github-dark-blue&hide_border=true)](https://github.com/kiikbye)
