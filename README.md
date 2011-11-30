# Compress CSS Files Using YUI Compressor & Apache ANT

## Usage:
    <!--S 引用CompressorCss目录下的project build.xml -->
    <target name="CompressCss">
        <!-- 可多此引用subant -->
        <subant>
            <property name="dir.source" value="${basedir}/test" />
            <property name="file.sources" value="*.css" />
            <property name="dir.output" value="${basedir}/test" />
            <property name="file.destname" value="css" />

            <fileset dir="./CompressorCss">
                <filename name="build.xml" />
            </fileset>
        </subant>
    </target>
    <!--E 引用CompressorCss目录下的project build.xml -->

## Arguments
    dir.source      [必须] 待压缩源目录
    file.sources     [可选] 待处理文件，可选，默认为目录下全部文件
    dir.output      [可选] 输出目录，可选，默认为同目录下的${dir.output}
    file.destname   [可选] 输出文件名称，默认为${file.destname}
