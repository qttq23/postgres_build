1. download Postgres binaries and unzip.  
at: `https://www.enterprisedb.com/download-postgresql-binaries`
or: `https://www.postgresql.org/download/windows/` and click to `zip archive`

2. download libpqxx source code and unzip.  
https://github.com/jtv/libpqxx/releases

3. create `libpqxx-7.7.3_build` and go to it.
mkdir build & cd build

4. config:
cmake -G "Visual Studio 17 2022" -A x64 -DPostgreSQL_ROOT="%cd%/../postgresql-14.4-1-windows-x64-binaries/pgsql" -DSKIP_BUILD_TEST=ON -DBUILD_SHARED_LIBS=OFF -DBUILD_DOC=OFF -DINSTALL_TEST=OFF "../libpqxx-7.7.3/libpqxx-7.7.3"

5. build:
cmake --build . --config Release

6. install 
cmake --install . --config Release --prefix "%cd%/../libpqxx-7.7.3_win32_x64_release"

