---
title: "Distributed File System"
date: 2024-03-15
draft: false
featured: true
weight: 80
thumbnail: "/thumbnails/bronco.jpg"
description: "A fault-tolerant distributed file system that distributes load across multiple machines, built as a group final project for Distributed Systems course."
technologies: ["Go", "Distributed Systems", "gRPC", "Fault Tolerance", "Replication"]
github: "https://github.com/roblee04/Distributed_File_System"
paper: "/files/Project_Report.pdf"
status: "Completed"
---

## Distributed File System

A group final project for my Distributed Systems course. We implemented a file system that could distribute load across many machines and handle failures gracefully.

### Key Features

- **Load Distribution**: Distributes file operations across multiple nodes
- **Fault Tolerance**: Handles node failures gracefully with automatic recovery
- **Replication**: Ensures data availability through replication
- **Scalability**: Designed to scale horizontally

### Technical Highlights

- Built with Go for performance and concurrency
- Uses gRPC for inter-node communication
- Implements distributed consensus algorithms
- Handles network partitions and node failures

### Project Report

<div style="margin: 2rem 0; padding: 1rem; background: #f5f5f5; border-radius: 8px;">
  <object data="/files/Project_Report.pdf" type="application/pdf" width="100%" height="600px">
    <p>Unable to display PDF file. <a href="/files/Project_Report.pdf">Download instead</a>.</p>
  </object>
</div>

[Download PDF →](/files/Project_Report.pdf)

### Source Code

[View on GitHub →](https://github.com/roblee04/Distributed_File_System)

### Team

This was a collaborative group project for the Distributed Systems course at Santa Clara University.