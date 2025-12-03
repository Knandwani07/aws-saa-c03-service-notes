# Amazon ElastiCache

---

## Overview

• Fully managed in-memory data store and cache service  
• Supports Redis and Memcached engines  
• Provides microsecond latency for real-time applications  
• Scales horizontally and vertically  
• Used for caching, session storage, real-time analytics  

---

## Key Benefits

• Reduces load on databases by caching frequent queries  
• Lowers latency and improves application performance  
• Fully managed: patching, setup, failure recovery handled by AWS  
• Supports multi-AZ with automatic failover (Redis)  

---

## Engines

• Redis  
- In-memory key-value store supporting data structures  
- Supports persistence (RDB and AOF)  
- Supports replication and automatic failover  
- Pub/Sub messaging capability  
- Advanced features like backups, cluster mode, multi-AZ  

• Memcached  
- Simple, in-memory key-value store  
- No persistence or replication  
- Supports sharding for horizontal scaling  
- Ideal for straightforward caching use cases  

---

## Architecture and Deployment

• Deployed into Amazon VPC  
• Nodes hosted on EC2 instances managed by AWS  
• Redis supports single-node, replica sets, and cluster mode  
• Multi-AZ deployments for high availability (Redis only)  
• Automatic backups (Redis)  
• Enhanced Monitoring and CloudWatch metrics  

---

## High Availability

• Redis: Supports replication groups with primary and replica nodes  
• Automatic failover to replica in case of primary node failure  
• Multi-AZ failover with minimal downtime  
• Backup and restore support for disaster recovery  

---

## Scaling

• Vertical scaling by changing node types  
• Horizontal scaling via sharding (Redis cluster mode, Memcached)  
• Add or remove nodes to meet demand  
• Supports online resharding in Redis cluster mode  

---

## Data Security

• Encryption in-transit using TLS  
• Encryption at-rest with AWS KMS (Redis)  
• IAM policies to control API access  
• Redis AUTH for password protection  
• VPC for network isolation and security groups for access control  

---

## Performance Features

• Microsecond latency reads and writes  
• Supports large datasets due to memory optimization  
• Connection multiplexing to reduce client connections  
• Optimized for high-throughput workloads  

---

## Backup and Restore (Redis Only)

• Supports automatic daily snapshots  
• Manual backups to Amazon S3  
• Restore clusters from snapshots  
• Useful for disaster recovery and migration  

---

## Monitoring and Management

• Amazon CloudWatch integration for metrics  
• Enhanced Monitoring for detailed metrics  
• AWS CLI, SDKs, Console for management  
• Events for operational changes and alerts  

---

## Integration with AWS Services

• Works with EC2, Lambda, RDS, DynamoDB, and more  
• Used to cache database query results  
• Can serve as a session store for stateless applications  
• Integrates with AWS CloudFormation for IaC  

---

## Use Cases

• Database query caching  
• Web session storage  
• Real-time analytics and leaderboards  
• Message brokering (Pub/Sub with Redis)  
• Gaming state management  
• Caching API responses  

---

## Pricing

• Pay for node hours based on instance type  
• Backup storage billed separately (Redis)  
• Data transfer within VPC free  
• Additional cost for multi-AZ, cluster mode  

---

## Best Practices

• Choose Redis for advanced features and persistence  
• Use Memcached for simple, ephemeral caching  
• Enable multi-AZ for production workloads needing HA  
• Use encryption in-transit and at-rest for sensitive data  
• Monitor usage with CloudWatch and scale nodes appropriately  
• Secure access with VPC, IAM, and Redis AUTH  

---

## Exam Tips

• Redis supports replication, backups, multi-AZ, cluster mode  
• Memcached is simpler, no replication or persistence  
• Multi-AZ is Redis-only with automatic failover  
• Encryption options available for Redis  
• Redis cluster mode enables horizontal partitioning  
• Use ElastiCache to reduce database load and improve latency  

---

## Quick Summary

Amazon ElastiCache is a fully managed, in-memory caching service that supports Redis and Memcached to deliver microsecond latency and high throughput for real-time applications. It provides automatic scaling, multi-AZ failover (Redis), encryption, and monitoring, making it ideal for caching, session management, real-time analytics, and reducing database load in scalable cloud architectures.

