---
title: "스키마 행 집합 클래스 및 Typedef 클래스 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vc.templates.ole"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "스키마 행 집합, 클래스"
ms.assetid: 4bd881b3-26ca-4bdb-9226-d67560864f29
caps.latest.revision: 6
caps.handback.revision: 6
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 스키마 행 집합 클래스 및 Typedef 클래스
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

A schema is a collection of database objects that are owned, or have been created by, a particular user.  A catalog can contain one or more schemas, but must always contain a schema called INFORMATION\_SCHEMA, which contains the views and domains of the information schema.  Schema information in OLE DB is retrieved using predefined schema rowsets, and includes types, tables, columns, indexes, views, assertions and constraints, statistics, character sets, collations, and domains.  
  
 Schema rowsets are predefined rowsets representing metadata.  Schema rowsets are generally used in dynamic programming, where the database structure is not known at compile time.  You can use these schema rowsets to obtain information about a database at run time.  
  
 Use the typedef classes to instantiate the schema rowsets.  The corresponding typedef and schema rowset classes are listed below.  You must call [CRestrictions::Open](../../data/oledb/crestrictions-open.md) after you have created an instance of the schema rowset.  This method returns a result set based on the restrictions you specify.  See [IDBSchemaRowset](https://msdn.microsoft.com/en-us/library/ms713686.aspx) for information on restriction columns associated with each schema rowset.  
  
 The following table displays each OLE DB Schema Rowset and its corresponding OLE DB Templates typedef class and info class.  
  
|OLE DB Schema Rowset|Typedef class|Info class|  
|--------------------------|-------------------|----------------|  
|[\<caps:sentence id\="tgt16" sentenceid\="ec22bc2607cdd42ce6fdd4a4e1a9dde0" class\="tgtSentence"\>ASSERTIONS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms719776.aspx)|[CAssertions](../../data/oledb/cassertions-cassertioninfo.md)|[CAssertionInfo](../../data/oledb/cassertions-cassertioninfo.md)|  
|[\<caps:sentence id\="tgt19" sentenceid\="666ff491210c66825be26d872dbef382" class\="tgtSentence"\>CATALOGS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms721241.aspx)|[CCatalogs](../../data/oledb/ccatalogs-ccataloginfo.md)|[CCatalogInfo](../../data/oledb/ccatalogs-ccataloginfo.md)|  
|[\<caps:sentence id\="tgt22" sentenceid\="75b164605d26f09aa0d59180f431ebe0" class\="tgtSentence"\>CHARACTER\_SETS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms722638.aspx)|[CCharacterSets](../../data/oledb/ccharactersets-ccharactersetinfo.md)|[CCharacterSetInfo](../../data/oledb/ccharactersets-ccharactersetinfo.md)|  
|[\<caps:sentence id\="tgt25" sentenceid\="1346fbfc7df7d1985877fff87577d626" class\="tgtSentence"\>COLLATIONS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms715783.aspx)|[CCollations](../../data/oledb/ccollations-ccollationinfo.md)|[CCollationInfo](../../data/oledb/ccollations-ccollationinfo.md)|  
|[\<caps:sentence id\="tgt28" sentenceid\="76717eb7707ef415936e8dd30d900648" class\="tgtSentence"\>COLUMN\_PRIVILEGES\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms715800.aspx)|[CColumnPrivileges](../../data/oledb/ccolumnprivileges-ccolumnprivilegeinfo.md)|[CColumnPrivilegeInfo](../../data/oledb/ccolumnprivileges-ccolumnprivilegeinfo.md)|  
|[\<caps:sentence id\="tgt31" sentenceid\="54ca84a794888fe8d92834787dfa935a" class\="tgtSentence"\>COLUMNS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms723052.aspx)|[CColumns](../../data/oledb/ccolumns-ccolumnsinfo.md)|[CColumnsInfo](../../data/oledb/ccolumns-ccolumnsinfo.md)|  
|[\<caps:sentence id\="tgt34" sentenceid\="04d425675b34ea772544500ae71868f6" class\="tgtSentence"\>CONSTRAINT\_COLUMN\_USAGE\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms724522.aspx)|[CConstraintColumnUsage](../../data/oledb/cconstraintcolumnusage-cconstraintcolumnusageinfo.md)|[CConstraintColumnUsageInfo](../../data/oledb/cconstraintcolumnusage-cconstraintcolumnusageinfo.md)|  
|[\<caps:sentence id\="tgt37" sentenceid\="bb12a1f03078e37b46b57d97d4f37a0c" class\="tgtSentence"\>CONSTRAINT\_TABLE\_USAGE\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms713710.aspx)|[CConstraintTableUsage](../../data/oledb/cconstrainttableusage-cconstrainttableusageinfo.md)|[CConstraintTableUsageInfo](../../data/oledb/cconstrainttableusage-cconstrainttableusageinfo.md)|  
|[\<caps:sentence id\="tgt40" sentenceid\="0792569fe8901b8e4f7dcd51f273911f" class\="tgtSentence"\>CHECK\_CONSTRAINTS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms712845.aspx)|[CCheckConstraints](../../data/oledb/ccheckconstraints-ccheckconstraintinfo.md)|[CCheckConstraintInfo](../../data/oledb/ccheckconstraints-ccheckconstraintinfo.md)|  
|[\<caps:sentence id\="tgt43" sentenceid\="c5b28210bee0ad75e7ab9d05baf43729" class\="tgtSentence"\>COLUMN\_DOMAIN\_USAGE\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms711240.aspx)|[CColumnDomainUsage](../../data/oledb/ccolumndomainusage-ccolumndomainusageinfo.md)|[CColumnDomainUsageInfo](../../data/oledb/ccolumndomainusage-ccolumndomainusageinfo.md)|  
|[\<caps:sentence id\="tgt46" sentenceid\="8a9c41f94b3adc0f8d72f69308561a98" class\="tgtSentence"\>FOREIGN\_KEYS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms711276.aspx)|[CForeignKeys](../../data/oledb/cforeignkeys-cforeignkeysinfo.md)|[CForeignKeysInfo](../../data/oledb/cforeignkeys-cforeignkeysinfo.md)|  
|[\<caps:sentence id\="tgt49" sentenceid\="626998f31a2e3a6b36816dcb3bb63ab3" class\="tgtSentence"\>INDEXES\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms709712.aspx)|[CIndexes](../../data/oledb/cindexes-cindexinfo.md)|[CIndexInfo](../../data/oledb/cindexes-cindexinfo.md)|  
|[\<caps:sentence id\="tgt52" sentenceid\="9995cd626fde05708549786a9076acc4" class\="tgtSentence"\>KEY\_COLUMN\_USAGE\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms712990.aspx)|[CKeyColumnUsage](../../data/oledb/ckeycolumns-ckeycolumninfo.md)|[CKeyColumnUsageInfo](../../data/oledb/ckeycolumns-ckeycolumninfo.md)|  
|[\<caps:sentence id\="tgt55" sentenceid\="b2aaf5199bd2b8b3d52f14dd089a13d1" class\="tgtSentence"\>PRIMARY\_KEYS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms714362.aspx)|[CPrimaryKeys](../../data/oledb/cprimarykeys-cprimarykeyinfo.md)|[CPrimaryKeyInfo](../../data/oledb/cprimarykeys-cprimarykeyinfo.md)|  
|[\<caps:sentence id\="tgt58" sentenceid\="c06924df8f6a6a11232e3ae804ce2bb3" class\="tgtSentence"\>PROCEDURES\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms724021.aspx)|[CProcedures](../../data/oledb/cprocedures-cprocedureinfo.md)|[CProcedureInfo](../../data/oledb/cprocedures-cprocedureinfo.md)|  
|[\<caps:sentence id\="tgt61" sentenceid\="32393213602aa1a11cf3265a8dc471e2" class\="tgtSentence"\>PROCEDURE\_COLUMNS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms723092.aspx)|[CProcedureColumns](../../data/oledb/cprocedurecolumns-cprocedurecolumninfo.md)|[CProcedureColumnInfo](../../data/oledb/cprocedurecolumns-cprocedurecolumninfo.md)|  
|[\<caps:sentence id\="tgt64" sentenceid\="900c36152da21b63960fc60b4acb2be2" class\="tgtSentence"\>PROCEDURE\_PARAMETERS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms713623.aspx)|[CProcedureParameters](../../data/oledb/cprocedureparameters-cprocedureparaminfo.md)|[CProcedureParameterInfo](../../data/oledb/cprocedureparameters-cprocedureparaminfo.md)|  
|[\<caps:sentence id\="tgt67" sentenceid\="b93a9987addb4bbb11de21b63ac1bb41" class\="tgtSentence"\>PROVIDER\_TYPES\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms709785.aspx)|[CProviderTypes](../../data/oledb/cprovidertypes-cproviderinfo.md)|[CProviderInfo](../../data/oledb/cprovidertypes-cproviderinfo.md)|  
|[\<caps:sentence id\="tgt70" sentenceid\="801a26b3b46b4f45bfc26d503cc3c9d0" class\="tgtSentence"\>REFERENTIAL\_CONSTRAINTS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms719737.aspx)|[CReferentialConstraints](../../data/oledb/creferentialconstraints-creferentialconstraintinfo.md)|[CReferentialConstraintInfo](../../data/oledb/creferentialconstraints-creferentialconstraintinfo.md)|  
|[\<caps:sentence id\="tgt73" sentenceid\="75384c1ef708add59deb323cb0610f3b" class\="tgtSentence"\>SCHEMATA\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms716887.aspx)|[CSchemata](../../data/oledb/cschemata-cschematainfo.md)|[CSchemataInfo](../../data/oledb/cschemata-cschematainfo.md)|  
|[\<caps:sentence id\="tgt76" sentenceid\="ec98845daab05b7fff258a8d3de0ce45" class\="tgtSentence"\>SQL\_LANGUAGES\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms714374.aspx)|[CSQLLanguages](../../data/oledb/csqllanguages-csqllanguageinfo.md)|[CSQLLanguageInfo](../../data/oledb/csqllanguages-csqllanguageinfo.md)|  
|[\<caps:sentence id\="tgt79" sentenceid\="a912a94d79b5124d876951f96ebb256f" class\="tgtSentence"\>STATISTICS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms715957.aspx)|[CStatistics](../../data/oledb/cstatistics-cstatisticinfo.md)|[CStatisticInfo](../../data/oledb/cstatistics-cstatisticinfo.md)|  
|[\<caps:sentence id\="tgt82" sentenceid\="7916f9a0d41ddf50399343fd9f51e309" class\="tgtSentence"\>TABLE\_CONSTRAINTS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms715921.aspx)|[CTableConstraints](../../data/oledb/ctableconstraints-ctableconstraintinfo.md)|[CTableConstraintInfo](../../data/oledb/ctableconstraints-ctableconstraintinfo.md)|  
|[\<caps:sentence id\="tgt85" sentenceid\="9ab2ec7ea4a2041306f7bdf150fcd453" class\="tgtSentence"\>TABLES\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms716980.aspx)|[CTables](../../data/oledb/ctables-ctableinfo.md)|[CTableInfo](../../data/oledb/ctables-ctableinfo.md)|  
|[\<caps:sentence id\="tgt88" sentenceid\="11daba2e66c06bd88c75f9e9052c437d" class\="tgtSentence"\>TABLE\_PRIVILEGES\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms725428.aspx)|[CTablePrivileges](../../data/oledb/ctableprivileges-ctableprivilegeinfo.md)|[CTablePrivilegeInfo](../../data/oledb/ctableprivileges-ctableprivilegeinfo.md)|  
|[\<caps:sentence id\="tgt91" sentenceid\="2ed18fafe4199c7cfc187fdb2a5b1a66" class\="tgtSentence"\>TRANSLATIONS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms725365.aspx)|[CTranslations](../../data/oledb/ctranslations-ctranslationinfo.md)|[CTranslationInfo](../../data/oledb/ctranslations-ctranslationinfo.md)|  
|[\<caps:sentence id\="tgt94" sentenceid\="f05363d8c209eb8bd0253f2a0effa2c4" class\="tgtSentence"\>USAGE\_PRIVILEGES\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms722743.aspx)|[CUsagePrivileges](../../data/oledb/cusageprivileges-cusageprivilegeinfo.md)|[CUsagePrivilegeInfo](../../data/oledb/cusageprivileges-cusageprivilegeinfo.md)|  
|[\<caps:sentence id\="tgt97" sentenceid\="ed42a0c4667e806c7c3d63cefa0306cb" class\="tgtSentence"\>VIEW\_COLUMN\_USAGE\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms714896.aspx)|[CViewColumnUsage](../../data/oledb/cviewcolumnusage-cviewcolumninfo.md)|[CViewColumnInfo](../../data/oledb/cviewcolumnusage-cviewcolumninfo.md)|  
|[\<caps:sentence id\="tgt100" sentenceid\="59a14a5786fe7a105d780bb1e1e2b21b" class\="tgtSentence"\>VIEWS\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms723122.aspx)|[CViews](../../data/oledb/cviews-cviewinfo.md)|[CViewInfo](../../data/oledb/cviews-cviewinfo.md)|  
|[\<caps:sentence id\="tgt103" sentenceid\="7bed95898597853c9b23a81f084d9253" class\="tgtSentence"\>VIEW\_TABLE\_USAGE\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms719727.aspx)|[CViewTableUsage](../../data/oledb/cviewtableusage-cviewtableinfo.md)|[CViewTableInfo](../../data/oledb/cviewtableusage-cviewtableinfo.md)|  
  
## 요구 사항  
 **Header:** atldbsch.h  
  
## 참고 항목  
 [CRestrictions 클래스](../../data/oledb/crestrictions-class.md)