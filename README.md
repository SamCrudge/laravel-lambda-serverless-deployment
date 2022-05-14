<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

# Steps to deploy

1. Install AWS SAM & serverless
```bash
brew tap aws/tap
brew install aws-sam-cli
npm install -g serverless
```
2. Deploy lambda infrastructure stack
```bash
# Deploy in 0.4-Building-A-Serverless-Laravel-App-With-AWS-SAM dir
cd 0.4-Building-A-Serverless-Laravel-App-With-AWS-SAM
sam deploy -g
```
5. Deploy serverless application onto infrastructure stack
```bash
# Deploy in root of application.
php artisan vendor:publish --tag=serverless-config
serverless deploy
```
