JPF����ִ�п��

�ļ��ṹ��
��ĿһĿǰ���������̹���һ�������ļ��ɣ�JPF-core, JPF-symbc, z3�Լ������ļ�site.properties
JPF-core: ���ڷ���ִ�е��ܿ�ܣ��ǻ���Java ��������Ŀ���չ�����������ܣ�����Ĺ��߶���������Ϊ������
JPF-symbc: ר�����ڷ���ִ�еĹ���
z3�������������ڲ��ԣ�����ỻ��greenSolver
site.properties ��ʽ���£�
# ע�⽫user.home�ĳɵ�ǰjpf�ļ��б���Ŀ¼
# JPF site configuration

jpf-core = ${user.home}/jpf/jpf-core

# numeric extension
jpf-numeric = ${user.home}/jpf/jpf-numeric

# annotation-based program properties extension
jpf-aprop = ${user.home}/jpf/jpf-aprop

extensions=${jpf-core},${jpf-aprop}

#... and all your other installed projects

�����������£�
��eclipse������
1.����jpf-core ��example
ʹ��eclipse ��װ��� ��ַ��http://babelfish.arc.nasa.gov/trac/jpf/raw-attachment/wiki/projects/eclipse-jpf/update
��src/examples ��ѡ���׺Ϊjpf���ļ��Ҽ�ѡ�� Verify... �Ϳ���������
2.����jpf-syboc��example
��ʼʱ�ᱨ���Ҳ���libz3java.dll,��java��classpath�м���Ŀ¼jpf/z3/build
��src/examples ��ѡ���׺Ϊjpf���ļ��Ҽ�ѡ�� Verify... �Ϳ���������

����������ִ��
> <jpf-core-dir>/bin/jpf +classpath=. <application-main-class>
����
> <jpf-core-dir>/bin/jpf <application-property-file>.jpf
����
> java -jar <jpf-core-dir>/build/RunJPF.jar +classpath=. <application-main-class>



