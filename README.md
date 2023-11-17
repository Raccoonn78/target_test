# Тестовое задание
### Выполнено



-- create table temp_group as (
-- SELECT 
-- COALESCE(x3,x2,x1) AS x ,
-- COALESCE(y3,y2,y1) AS y,
-- COALESCE(z3,z2,z1) AS z   ,
-- COALESCE(m3,m2,m1) AS mm   ,
-- COALESCE(n3,n2,n1) AS n   ,
-- COALESCE(p3,p2,p1) AS pp   ,
-- COALESCE(o3,o2,o1) AS o   ,
-- SUM(val)  as val
-- FROM zxc2
-- GROUP BY y1,y2,y3,z1,z2,z3,m1,m2,m3,n1,n2,n3,p1,p2,p3,o1,o2,o3, CUBE (x1,x2,x3) );

-- insert into temp_group 
-- SELECT 
-- COALESCE(x3,x2,x1) AS x ,
-- COALESCE(y3,y2,y1) AS y,
-- COALESCE(z3,z2,z1) AS z   ,
-- COALESCE(m3,m2,m1) AS mm   ,
-- COALESCE(n3,n2,n1) AS n   ,
-- COALESCE(p3,p2,p1) AS pp   ,
-- COALESCE(o3,o2,o1) AS o   ,
-- SUM(val)  as val
-- FROM zxc2
-- GROUP BY x1,x2,x3,z1,z2,z3,m1,m2,m3,n1,n2,n3,p1,p2,p3,o1,o2,o3, CUBE (y1,y2,y3);


-- insert into temp_group 
-- SELECT 
-- COALESCE(x3,x2,x1) AS x ,
-- COALESCE(y3,y2,y1) AS y,
-- COALESCE(z3,z2,z1) AS z   ,
-- COALESCE(m3,m2,m1) AS mm   ,
-- COALESCE(n3,n2,n1) AS n   ,
-- COALESCE(p3,p2,p1) AS pp   ,
-- COALESCE(o3,o2,o1) AS o   ,
-- SUM(val)  as val
-- FROM zxc2
-- GROUP BY x1,x2,x3,y1,y2,y3,m1,m2,m3,n1,n2,n3,p1,p2,p3,o1,o2,o3, CUBE (z1,z2,z3);


-- insert into temp_group 
-- SELECT 
-- COALESCE(x3,x2,x1) AS x ,
-- COALESCE(y3,y2,y1) AS y,
-- COALESCE(z3,z2,z1) AS z   ,
-- COALESCE(m3,m2,m1) AS mm   ,
-- COALESCE(n3,n2,n1) AS n   ,
-- COALESCE(p3,p2,p1) AS pp   ,
-- COALESCE(o3,o2,o1) AS o   ,
-- SUM(val)  as val
-- FROM zxc2
-- GROUP BY x1,x2,x3,y1,y2,y3,z1,z2,z3,n1,n2,n3,p1,p2,p3,o1,o2,o3, CUBE (m1,m2,m3);


-- insert into temp_group 
-- SELECT 
-- COALESCE(x3,x2,x1) AS x ,
-- COALESCE(y3,y2,y1) AS y,
-- COALESCE(z3,z2,z1) AS z   ,
-- COALESCE(m3,m2,m1) AS mm   ,
-- COALESCE(n3,n2,n1) AS n   ,
-- COALESCE(p3,p2,p1) AS pp   ,
-- COALESCE(o3,o2,o1) AS o   ,
-- SUM(val)  as val
-- FROM zxc2
-- GROUP BY x1,x2,x3,y1,y2,y3,z1,z2,z3,m1,m2,m3,p1,p2,p3,o1,o2,o3, CUBE (n1,n2,n3);


-- insert into temp_group 
-- SELECT 
-- COALESCE(x3,x2,x1) AS x ,
-- COALESCE(y3,y2,y1) AS y,
-- COALESCE(z3,z2,z1) AS z   ,
-- COALESCE(m3,m2,m1) AS mm   ,
-- COALESCE(n3,n2,n1) AS n   ,
-- COALESCE(p3,p2,p1) AS pp   ,
-- COALESCE(o3,o2,o1) AS o   ,
-- SUM(val)  as val
-- FROM zxc2
-- GROUP BY x1,x2,x3,y1,y2,y3,z1,z2,z3,m1,m2,m3,n1,n2,n3,o1,o2,o3, CUBE (p1,p2,p3);



-- insert into temp_group 
-- SELECT 
-- COALESCE(x3,x2,x1) AS x ,
-- COALESCE(y3,y2,y1) AS y,
-- COALESCE(z3,z2,z1) AS z   ,
-- COALESCE(m3,m2,m1) AS mm   ,
-- COALESCE(n3,n2,n1) AS n   ,
-- COALESCE(p3,p2,p1) AS pp   ,
-- COALESCE(o3,o2,o1) AS o   ,
-- SUM(val)  as val
-- FROM zxc2
-- GROUP BY x1,x2,x3,y1,y2,y3,z1,z2,z3,m1,m2,m3,n1,n2,n3,p1,p2,p3,o1,o2,o3, CUBE (o1,o2,o3);












-- create table index_union as (
-- select LPAD( n1.indexx,7, '0') as x , LPAD( n2.indexx,7, '0') as y 
-- , COALESCE( LPAD( n3.indexx,7, '0'),'0000000') as z , LPAD( n4.indexx,7, '0') as mm 
-- , LPAD( n5.indexx,7, '0') as n  ,LPAD( n6.indexx,7, '0') as o 
-- , LPAD( n7.indexx,7, '0') as pp ,
-- concat_ws ('', COALESCE(LPAD( n1.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n2.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n3.indexx,7, '0'),'0000000'), 
-- 		   	 COALESCE(LPAD( n4.indexx,7, '0'),'0000000'),
-- 		 	 COALESCE(LPAD( n5.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n6.indexx,7, '0') ,'0000000'),
-- 		   	 COALESCE(LPAD( n7.indexx,7, '0'),'0000000')  ,'00000'    ) as INDEXXXXX, val
-- from temp_group 
-- LEFT JOIN nodes_df n1 ON temp_group.x=n1.namee  
-- LEFT JOIN nodes_df n2 ON temp_group.y=n2.namee
-- LEFT JOIN nodes_df n3 ON temp_group.z=n3.namee
-- LEFT JOIN nodes_df n4 ON temp_group.mm=n4.namee
-- LEFT JOIN nodes_df n5 ON temp_group.n=n5.namee
-- LEFT JOIN nodes_df n6 ON temp_group.o=n6.namee
-- LEFT JOIN nodes_df n7 ON temp_group.pp=n7.namee
-- UNION 
-- select LPAD( n1.indexx,7, '0') as x , LPAD( n2.indexx,7, '0') as y 
-- , COALESCE( LPAD( n3.indexx,7, '0'),'0000000') as z , LPAD( n4.indexx,7, '0') as mm 
-- , LPAD( n5.indexx,7, '0') as n  ,LPAD( n6.indexx,7, '0') as o 
-- , LPAD( n7.indexx,7, '0') as pp ,
-- concat_ws ('', COALESCE(LPAD( n1.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n2.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n3.indexx,7, '0'),'0000000'), 
-- 		   	 COALESCE(LPAD( n4.indexx,7, '0'),'0000000'),
-- 		 	 COALESCE(LPAD( n5.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n6.indexx,7, '0') ,'0000000'),
-- 		   	 COALESCE(LPAD( n7.indexx,7, '0'),'0000000')  ,'11111'    ) as INDEXXXXX, val
-- from temp_group 
-- LEFT JOIN nodes_df n1 ON temp_group.x=n1.namee  
-- LEFT JOIN nodes_df n2 ON temp_group.y=n2.namee
-- LEFT JOIN nodes_df n3 ON temp_group.z=n3.namee
-- LEFT JOIN nodes_df n4 ON temp_group.mm=n4.namee
-- LEFT JOIN nodes_df n5 ON temp_group.n=n5.namee
-- LEFT JOIN nodes_df n6 ON temp_group.o=n6.namee
-- LEFT JOIN nodes_df n7 ON temp_group.pp=n7.namee
-- UNION 
-- select LPAD( n1.indexx,7, '0') as x , LPAD( n2.indexx,7, '0') as y 
-- , COALESCE( LPAD( n3.indexx,7, '0'),'0000000') as z , LPAD( n4.indexx,7, '0') as mm 
-- , LPAD( n5.indexx,7, '0') as n  ,LPAD( n6.indexx,7, '0') as o 
-- , LPAD( n7.indexx,7, '0') as pp ,
-- concat_ws ('', COALESCE(LPAD( n1.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n2.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n3.indexx,7, '0'),'0000000'), 
-- 		   	 COALESCE(LPAD( n4.indexx,7, '0'),'0000000'),
-- 		 	 COALESCE(LPAD( n5.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n6.indexx,7, '0') ,'0000000'),
-- 		   	 COALESCE(LPAD( n7.indexx,7, '0'),'0000000')  ,'22222'    ) as INDEXXXXX, val
-- from temp_group 
-- LEFT JOIN nodes_df n1 ON temp_group.x=n1.namee  
-- LEFT JOIN nodes_df n2 ON temp_group.y=n2.namee
-- LEFT JOIN nodes_df n3 ON temp_group.z=n3.namee
-- LEFT JOIN nodes_df n4 ON temp_group.mm=n4.namee
-- LEFT JOIN nodes_df n5 ON temp_group.n=n5.namee
-- LEFT JOIN nodes_df n6 ON temp_group.o=n6.namee
-- LEFT JOIN nodes_df n7 ON temp_group.pp=n7.namee

-- UNION 
-- select LPAD( n1.indexx,7, '0') as x , LPAD( n2.indexx,7, '0') as y 
-- , COALESCE( LPAD( n3.indexx,7, '0'),'0000000') as z , LPAD( n4.indexx,7, '0') as mm 
-- , LPAD( n5.indexx,7, '0') as n  ,LPAD( n6.indexx,7, '0') as o 
-- , LPAD( n7.indexx,7, '0') as pp ,
-- concat_ws ('', COALESCE(LPAD( n1.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n2.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n3.indexx,7, '0'),'0000000'), 
-- 		   	 COALESCE(LPAD( n4.indexx,7, '0'),'0000000'),
-- 		 	 COALESCE(LPAD( n5.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n6.indexx,7, '0') ,'0000000'),
-- 		   	 COALESCE(LPAD( n7.indexx,7, '0'),'0000000')  ,'33333'    ) as INDEXXXXX, val
-- from temp_group 
-- LEFT JOIN nodes_df n1 ON temp_group.x=n1.namee  
-- LEFT JOIN nodes_df n2 ON temp_group.y=n2.namee
-- LEFT JOIN nodes_df n3 ON temp_group.z=n3.namee
-- LEFT JOIN nodes_df n4 ON temp_group.mm=n4.namee
-- LEFT JOIN nodes_df n5 ON temp_group.n=n5.namee
-- LEFT JOIN nodes_df n6 ON temp_group.o=n6.namee
-- LEFT JOIN nodes_df n7 ON temp_group.pp=n7.namee

-- UNION 
-- select LPAD( n1.indexx,7, '0') as x , LPAD( n2.indexx,7, '0') as y 
-- , COALESCE( LPAD( n3.indexx,7, '0'),'0000000') as z , LPAD( n4.indexx,7, '0') as mm 
-- , LPAD( n5.indexx,7, '0') as n  ,LPAD( n6.indexx,7, '0') as o 
-- , LPAD( n7.indexx,7, '0') as pp ,
-- concat_ws ('', COALESCE(LPAD( n1.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n2.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n3.indexx,7, '0'),'0000000'), 
-- 		   	 COALESCE(LPAD( n4.indexx,7, '0'),'0000000'),
-- 		 	 COALESCE(LPAD( n5.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n6.indexx,7, '0') ,'0000000'),
-- 		   	 COALESCE(LPAD( n7.indexx,7, '0'),'0000000')  ,'44444'    ) as INDEXXXXX, val
-- from temp_group 
-- LEFT JOIN nodes_df n1 ON temp_group.x=n1.namee  
-- LEFT JOIN nodes_df n2 ON temp_group.y=n2.namee
-- LEFT JOIN nodes_df n3 ON temp_group.z=n3.namee
-- LEFT JOIN nodes_df n4 ON temp_group.mm=n4.namee
-- LEFT JOIN nodes_df n5 ON temp_group.n=n5.namee
-- LEFT JOIN nodes_df n6 ON temp_group.o=n6.namee
-- LEFT JOIN nodes_df n7 ON temp_group.pp=n7.namee

-- UNION 
-- select LPAD( n1.indexx,7, '0') as x , LPAD( n2.indexx,7, '0') as y 
-- , COALESCE( LPAD( n3.indexx,7, '0'),'0000000') as z , LPAD( n4.indexx,7, '0') as mm 
-- , LPAD( n5.indexx,7, '0') as n  ,LPAD( n6.indexx,7, '0') as o 
-- , LPAD( n7.indexx,7, '0') as pp ,
-- concat_ws ('', COALESCE(LPAD( n1.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n2.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n3.indexx,7, '0'),'0000000'), 
-- 		   	 COALESCE(LPAD( n4.indexx,7, '0'),'0000000'),
-- 		 	 COALESCE(LPAD( n5.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n6.indexx,7, '0') ,'0000000'),
-- 		   	 COALESCE(LPAD( n7.indexx,7, '0'),'0000000')  ,'55555'    ) as INDEXXXXX, val
-- from temp_group 
-- LEFT JOIN nodes_df n1 ON temp_group.x=n1.namee  
-- LEFT JOIN nodes_df n2 ON temp_group.y=n2.namee
-- LEFT JOIN nodes_df n3 ON temp_group.z=n3.namee
-- LEFT JOIN nodes_df n4 ON temp_group.mm=n4.namee
-- LEFT JOIN nodes_df n5 ON temp_group.n=n5.namee
-- LEFT JOIN nodes_df n6 ON temp_group.o=n6.namee
-- LEFT JOIN nodes_df n7 ON temp_group.pp=n7.namee

-- UNION 
-- select LPAD( n1.indexx,7, '0') as x , LPAD( n2.indexx,7, '0') as y 
-- , COALESCE( LPAD( n3.indexx,7, '0'),'0000000') as z , LPAD( n4.indexx,7, '0') as mm 
-- , LPAD( n5.indexx,7, '0') as n  ,LPAD( n6.indexx,7, '0') as o 
-- , LPAD( n7.indexx,7, '0') as pp ,
-- concat_ws ('', COALESCE(LPAD( n1.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n2.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n3.indexx,7, '0'),'0000000'), 
-- 		   	 COALESCE(LPAD( n4.indexx,7, '0'),'0000000'),
-- 		 	 COALESCE(LPAD( n5.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n6.indexx,7, '0') ,'0000000'),
-- 		   	 COALESCE(LPAD( n7.indexx,7, '0'),'0000000')  ,'66666'    ) as INDEXXXXX, val
-- from temp_group 
-- LEFT JOIN nodes_df n1 ON temp_group.x=n1.namee  
-- LEFT JOIN nodes_df n2 ON temp_group.y=n2.namee
-- LEFT JOIN nodes_df n3 ON temp_group.z=n3.namee
-- LEFT JOIN nodes_df n4 ON temp_group.mm=n4.namee
-- LEFT JOIN nodes_df n5 ON temp_group.n=n5.namee
-- LEFT JOIN nodes_df n6 ON temp_group.o=n6.namee
-- LEFT JOIN nodes_df n7 ON temp_group.pp=n7.namee

-- UNION 
-- select LPAD( n1.indexx,7, '0') as x , LPAD( n2.indexx,7, '0') as y 
-- , COALESCE( LPAD( n3.indexx,7, '0'),'0000000') as z , LPAD( n4.indexx,7, '0') as mm 
-- , LPAD( n5.indexx,7, '0') as n  ,LPAD( n6.indexx,7, '0') as o 
-- , LPAD( n7.indexx,7, '0') as pp ,
-- concat_ws ('', COALESCE(LPAD( n1.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n2.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n3.indexx,7, '0'),'0000000'), 
-- 		   	 COALESCE(LPAD( n4.indexx,7, '0'),'0000000'),
-- 		 	 COALESCE(LPAD( n5.indexx,7, '0'),'0000000'),
-- 		   	 COALESCE(LPAD( n6.indexx,7, '0') ,'0000000'),
-- 		   	 COALESCE(LPAD( n7.indexx,7, '0'),'0000000')  ,'77777'    ) as INDEXXXXX, val
-- from temp_group 
-- LEFT JOIN nodes_df n1 ON temp_group.x=n1.namee  
-- LEFT JOIN nodes_df n2 ON temp_group.y=n2.namee
-- LEFT JOIN nodes_df n3 ON temp_group.z=n3.namee
-- LEFT JOIN nodes_df n4 ON temp_group.mm=n4.namee
-- LEFT JOIN nodes_df n5 ON temp_group.n=n5.namee
-- LEFT JOIN nodes_df n6 ON temp_group.o=n6.namee
-- LEFT JOIN nodes_df n7 ON temp_group.pp=n7.namee

