<div align="center">
  
  # AWS-prestashop-deployment
  
  # PrestaShop 8.1.2 E-Commerce Platform Deployed on AWS Free Tier with Separated Application and Database Architecture.

</div>

## Project Summary
This hands-on lab demonstrates the deployment of a **fully functional PrestaShop 8.1.2 e-commerce store** using **only AWS Free Tier resources**, with complete separation of the application layer (EC2) and database layer (RDS) — following industry best practices for scalability and security.

**Key Objectives**
- Deploy PrestaShop using strictly Free Tier eligible resources (no charges incurred)
- Maintain clear separation between application server and database
- Achieve a publicly accessible, production-ready storefront


**Solution Delivered**
- EC2 t3.micro running Ubuntu 22.04 LTS + LAMP stack
- Dedicated RDS db.t3.micro MySQL instance
- PrestaShop 8.1.2 with default theme and demo products
- Proper security groups, permissions, and post-install hardening

## Architecture Delivered
- **Application Server**: EC2 t3.micro (Ubuntu 22.04 LTS) – Public IP: `16.171.38.133`
- **Database**: RDS db.t3.micro MySQL 8.0 (isolated instance)
- **Web Stack**: Apache 2 + PHP 8.3 + required modules
- **File Share/Storage**: PrestaShop files hosted on EC2 root volume
- **Security**: Custom security groups, public access enabled only for HTTP/SSH, RDS accessible only from EC2

**Live Store**: [http://16.171.38.133/index.php](http://16.171.38.133/index.php)

## Validation Results
| Test Case                          | Expected Outcome               | Result |
|------------------------------------|--------------------------------|--------|
| LAMP stack installation            | Apache default page loads      | ✅     |
| PrestaShop files deployment        | Correct ownership & permissions| ✅     |
| RDS database connection test       | Successful MySQL login         | ✅     |
| PrestaShop web installer           | Database & shop configuration  | ✅     |
| Final storefront access            | Demo products & theme visible  | ✅     |
| Public internet accessibility      | Store loads without issues     | ✅     |

## Full Documentation
📄 **Complete Lab Report (PDF)**  
[Open / View Full Report (PDF)](https://raw.githubusercontent.com/yourusername/prestashop-aws-free-tier/main/docs/PrestaShop-AWS-Free-Tier-Full-Report.pdf)  

*(Replace `yourusername` with your GitHub username and upload the original PDF to the `docs/` folder)*

## Screenshots (Visual Evidence)
All 14 high-resolution screenshots are available in the [`screenshots/`](./screenshots/) folder:

1. EC2 instance launch  
2. Security group & key pair configuration  
3. SSH connection & LAMP stack installation  
4. Apache default page verification  
5. PrestaShop zip download & extraction  
6. RDS database creation  
7. RDS endpoint & security group setup  
8. MySQL client connection test  
9. PrestaShop installer – database configuration  
10. Shop details & installation progress  
11. Successful installation confirmation  
12. Final storefront with demo products  
 

## Challenges & Resolutions
- Permission errors during file extraction → resolved with proper `chown` and `chmod` commands  
- RDS connectivity issues → verified security group rules and used correct endpoint  
- Installer timeout → increased PHP execution time and confirmed MySQL driver  
- All issues documented with screenshots for future reference

## Conclusion
This project successfully delivers a complete, production-grade PrestaShop e-commerce platform on AWS Free Tier while maintaining strict separation between application and database layers. The solution is fully documented, visually validated, and ready for production scaling.



