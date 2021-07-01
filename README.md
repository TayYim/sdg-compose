# sdg-compose

Clone carla-autoware project
```
git clone git@codeup.aliyun.com:5f3f374f6207a1a8b17f933f/SelfDriveGuard/carla-autoware.git

cd carla-autoware

wget -c https://guard-strike.oss-cn-shanghai.aliyuncs.com/ADTest/autoware-contents.zip

unzip autoware-contents.zip

rm autoware-contents.zip
```

Make sure you have carla-autoware-extern image
```
docker pull registry.cn-beijing.aliyuncs.com/ad-test/carla-autoware-extern:1.0.1
```

Build carla-autoware-sdg image
```
cd carla-autoware

docker build -t carla-autoware-sdg -f Dockerfile_sdg .
```

Pull carlasim image
```
docker pull registry.cn-beijing.aliyuncs.com/ad-test/carlasim:0.9.10
```

Pull sdg engine image
```
docker pull registry.cn-beijing.aliyuncs.com/selfdriveguard/sdg-engine
```

Run
```
docker-sompose up
```