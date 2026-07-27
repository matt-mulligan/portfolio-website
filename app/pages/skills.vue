<script setup lang="ts">
  const skillsEntries = [
    {
      heading: 'Core Skills',
      sections: [
        {
          subtitle: 'System Design',
          details: [
            'Architecting distributed systems, event-driven applications, and microservice ecosystems',
            'Designing resilient, scalable solutions with a focus on performance, reliability, and maintainability',
          ],
        },
        {
          subtitle: 'Software Engineering',
          details: [
            'Writing clean, maintainable, and well-tested software following modern engineering best practices',
            'Driving software quality through automated testing, code reviews, and continuous integration',
            'Applying SOLID principles, design patterns, and clean code methodologies across complex codebases',
          ],
        },
        {
          subtitle: 'Data Engineering',
          details: [
            'Designing and building scalable data pipelines for batch and real-time data processing',
            'Optimising large-scale data processing through partitioning, indexing, caching, and query tuning',
            'Building reliable data platforms with a focus on data quality, governance, and operational excellence',
          ],
        },
        {
          subtitle: 'Technical Leadership',
          details: [
            'Leading technical design discussions and driving architecture decisions across cross-functional teams',
            'Mentoring engineers and promoting engineering best practices through collaboration and knowledge sharing',
            'Translating business requirements into scalable technical solutions and engineering roadmaps',
          ],
        }
      ],
    },
    {
      heading: 'Programming Languages',
      sections: [
        {
          subtitle: 'Python',
          details: [
            '7+ years experience',
            'Modern Python (3.11+), writing clean, modular, maintainable, and type-safe code following best practices and PEP standards',
            'Automated testing and code quality using pytest, mypy, Ruff, Black, and CI/CD pipelines to ensure reliable, production-ready software.',
            'Asynchronous programming with asyncio, concurrent processing, and performance optimisation for I/O-intensive applications',
            'Backend API development using FastAPI with experience building scalable RESTful services',
          ],
        },
        {
          subtitle: 'Spark/Spark Connect',
          details: [
            '7+ years experience',
            'Distributed data processing using Apache Spark and PySpark to build scalable ETL and data transformation pipelines',
            'Designed end to end data processing frameworks to support large-scale data analytics and machine learning applications',
            'Built and supported batch, micro-batch and streaming data processing pipelines through to production',
            'Performance optimisation through partitioning, caching, broadcast joins, predicate pushdown, and efficient execution plan tuning',
            'Delivering production-grade data platforms with monitoring, testing, CI/CD, and fault-tolerant distributed processing on Azure'
          ]
        },
        {
          subtitle: 'Golang',
          details: [
            '1+ years experience',
            'Backend development in Go, building high-performance, scalable, and maintainable microservices using idiomatic Go practices',
            'RESTful and gRPC API development, designing secure, efficient, and well-documented backend services',
          ]
        },
      ],
    },
    {
      heading: 'Platforms',
      sections: [
        {
          subtitle: '',
          details: [
            'Hadoop (HDFS, Hive, Atlas, YARN, HBase, Phoenix)',
            'Azure Cloud (ADLS, AKV, AKS, CosmosDB, AEH)',
            'AWS (S3, DynamoDB, EC2, Lambda, SQS)',
            'Automation/CICD (Jenkins, Terraform, Github Actions)',
          ],
        },
      ],
    },
  ];
</script>

<template>
  <div>
    <h1 class="page-title">Skills</h1>

    <SkillsEntry v-for="entry in skillsEntries" :key="entry.heading" v-bind="entry" />
  </div>
</template>
