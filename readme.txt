                 HiKariʹ��˵��
�����ʼ��
  ʹ��������
   HikariConfig hikariConfig = new HikariConfig();
            hikariConfig.DBType = "PostgreSQL";
            hikariConfig.ConnectString = "Server = 127.0.0.1; Port = 5432; User Id = postgres; Password = 1234; Database = postgres;Pooling=true; ";
            hikariConfig.DriverDir = "DBDrivers";
            hikariConfig.DriverDLL = "XXXX.dll";
            hikariConfig.DBTypeXml = "DBType.xml";

            HikariDataSource hikariDataSource = new HikariDataSource(hikariConfig);

ֱ��ʹ��
  HikariDataSource hikariDataSource = new HikariDataSource();
            hikariDataSource.DBType = "PostgreSQL";
            hikariDataSource.ConnectString = "Server = 127.0.0.1; Port = 5432; User Id = postgres; Password = 1234; Database = postgres;Pooling=true; ";
            hikariDataSource.DriverDir = "DBDrivers";
            hikariDataSource.DriverDLL = "XXXX.dll";
            hikariDataSource.DBTypeXml = "DBType.xml";

�����ļ�
HikariConfig hikariConfig = new HikariConfig();
hikariConfig.LoadConfig("Hikari.txt");
//Ҳ����ʹ��
HikariDataSource hikariDataSource = new HikariDataSource();
            hikariDataSource.LoadConfig("Hikari.txt");

ʹ��
hikariDataSource.GetConnection();

˵��������������ã����������DLL.
����dll���ҵ�·����DriverDir+ DriverDLL������һ��Ҫ���úá�
����һ���ǣ������û�����ã�����������DBType.���򽫻����DBTypeȥ����dll���ƣ��Զ�ȥ����DriverDLL��
DBType������д����4�֣�����¼��
������ȡDBType.xml�ļ�����ȡȫ��������Ϣ���������ļ�������Ϣ�������ڳ���������HikariConfig����HikariDataSource��DBTypeXml���ԡ�


Դ���˵
HikariDataSource �����ṩ����
HikariConfig ��������
HikariPool ����������ϣ�������Դ
PoolBase �����������ӣ���HikariPool����


��¼
���ݿ�	Dll����	˵��
Oracle	Oracle.ManagedDataAccess	��ǰ�������dll
MySql	MySql.Data	
SqlServer	System	
PostgreSQL	Npgsql	

