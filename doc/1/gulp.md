
#####安装 gulp
    npm install --save-dev gulp
#####安装 gulp-sass
    npm install --save-dev gulp-sass
#####创建gulpfile.js
    var gulp = require('gulp');
    var sass = require('gulp-sass');
    
    // 编译scss文件
    gulp.task('sass', function () {
        return gulp.src('./sass/**/[^_]*.scss')
            .pipe(sass().on('error', sass.logError))
            .pipe(gulp.dest('./css'));
    });
    
    gulp.task('sass:watch', function () {
        gulp.watch('./sass/**/*.scss', ['sass']);
    });