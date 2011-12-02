# Compress CSS Files Using YUI Compressor & Apache ANT

## Usage:
    <!--S 引用CompressorCss目录下的project build.xml -->
    <target name="CompressCss">
        <!-- 可多此引用subant -->
        <subant>
            <property name="dir.source" value="${basedir}/test" />
            <property name="dir.output" value="${basedir}/test" />
            <property name="file.destname" value="css" />
            <property name="file.includes" value="*.css" />
            <property name="file.excludes" value="tmp.css," />

            <fileset dir="./CompressorCss">
                <filename name="build.xml" />
            </fileset>
        </subant>
    </target>
    <!--E 引用CompressorCss目录下的project build.xml -->

## Arguments
    dir.source      [必须] 待压缩源目录
    file.includes   [可选] 待处理文件，可选，默认为目录下全部文件
    file.excludes   [可选] 不匹配列表，默认为${file.destname}.min.css（压缩过的文件)
    dir.output      [可选] 输出目录，可选，默认为同目录下的${dir.output}
    file.destname   [可选] 输出文件名称，默认为${file.destname}
