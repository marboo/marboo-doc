#!/usr/bin/env rake -f
# coding: utf-8
# file name: Rakefile
# description: TODO
# author: amoblin
# create date: 2015-08-16 09:19:02
# This file is created by Marboo<http://marboo.io> template file $MARBOO_HOME/.media/starts/Rakefile
# 本文件由 Marboo<http://marboo.io> 模板文件 $MARBOO_HOME/.media/starts/Rakefile　创建

task :default do |t|
  sh "gitbook build"
  sh "gitbook epub"
  sh "gitbook pdf"
end

task :update do |t|
  sh "git pull --unshallow"
end

task :clean do |t|
  sh "find . -name .DS_Store|xargs rm -f"
end
