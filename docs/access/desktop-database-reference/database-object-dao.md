---
title: Objet de base de données (DAO)
TOCTitle: Database Object
ms:assetid: 6cf2ddf8-3957-a15e-5eeb-85f81c1e415e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195520(v=office.15)
ms:contentKeyID: 48545482
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm0
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 265edf6b5d426b87d718c66e9886b7a4877120de
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918848"
---
# <a name="database-object-dao"></a>Objet de base de données (DAO)

**S’applique à**: Access 2013, Office 2013

Un objet **Database** représente une base de données ouverte.

## <a name="remarks"></a>Remarques

L'objet **Database**, ainsi que ses méthodes et propriétés, permet de manipuler une base de données ouverte. Dans tous les types de base de données, vous pouvez :

  - Utiliser la méthode **Execute** pour exécuter une requête d'action.

  - Définir la propriété **Connect** pour établir une connexion avec une source de données ODBC.

  - Définir la propriété **QueryTimeout** pour limiter le temps d'attente pour l'exécution d'une requête dans une source de données ODBC.

  - Utiliser la propriété **RecordsAffected** pour déterminer le nombre d'enregistrements qui ont été modifiés par une requête Action.

  - Utiliser la méthode **OpenRecordset** pour exécuter une requête Select et créer un objet **Recordset**.

  - Utiliser la propriété **Version** pour déterminer la version de moteur de base de données qui a créé la base de données.

Avec une base de données de moteur de base de données Microsoft Access, vous pouvez également utiliser d'autres méthodes, propriétés et collections pour manipuler un objet **Database**, mais aussi créer, modifier ou obtenir des informations se rapportant à ses tables, requêtes et relations. Par exemple, vous pouvez :

  - Utiliser les méthodes **CreateTableDef** et **CreateRelation** pour créer respectivement des tables et des relations.

  - Utiliser la méthode **CreateProperty** pour définir de nouvelles propriétés **Database**.

  - Utiliser la méthode **CreateQueryDef** pour créer une définition de requête persistante ou temporaire.

  - Utiliser les méthodes **MakeReplica**, **Synchronize** et **PopulatePartial** pour créer et synchroniser des réplicas partiels ou complets de votre base de données.

  - Définir la propriété **CollatingOrder** pour définir l'ordre de tri alphabétique des champs de caractères dans différentes langues.

Vous utilisez la méthode **CreateDatabase** pour créer un objet **Database** persistant, qui est automatiquement ajouté à la collection **Databases**, et donc pour l'enregistrer sur le disque.

Vous n'avez pas besoin de spécifier l'objet **DBEngine** lorsque vous utilisez la méthode **OpenDatabase**.

L'ouverture d'une base de données avec des tables liées ne définit pas automatiquement des liaisons vers les fichiers externes spécifiés. Vous devez référencer les objets **TableDef** ou **Field** de la table, ou ouvrir un objet **Recordset**. Si vous ne pouvez pas définir de liaisons vers ces tables, une erreur pouvant être interceptée se produit.

Lorsqu'une procédure qui déclare un objet **Database** a été exécutée, les objets **Database** locaux sont fermés avec les objets **Recordset** ouverts. Toutes les mises à jour en attente sont perdues et les transactions en attente sont annulées, mais aucune erreur pouvant être interceptée ne se produit. Vous devez terminer explicitement les transactions en attente ou modifier et fermer les objets **Recordset** et **Database** avant de quitter les procédures qui déclarent ces variables d'objet localement.

Lorsque vous utilisez l’une des méthodes de transaction (**BeginTrans**, **CommitTrans** ou **Rollback**) dans l’objet **Workspace**, ces transactions s’appliquent à toutes les bases de données ouvertes dans l’objet **Workspace** dans lequel l’objet **Database** a été ouvert. Si vous souhaitez utiliser des transactions indépendantes, vous devez d’abord ouvrir un autre objet **Workspace**, puis ouvrir un autre objet **Database** dans cet objet **Workspace**.


> [!NOTE]
> [!REMARQUE] Vous pouvez ouvrir la même source ou base de données plusieurs fois, ce qui crée des noms dupliqués dans la collection **Databases**. Il convient d'affecter des objets **Database** aux variables d'objet et de s'y référer par nom de variables.



## <a name="example"></a>Exemple

Cet exemple crée un objet **Database** et ouvre un objet **Database** existant dans l'objet **Workspace** par défaut. Ensuite, il énumère la collection **Database** et la collection **Properties** de chaque objet **Database**.

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccessWorkspace", "admin", _ 
 "", dbUseJet) 
 
 ' Make sure there isn't already a file with the name of 
 ' the new database. 
 If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
 
 ' Create a new database with the specified 
 ' collating order. 
 Set dbsNew = wrkAcc.CreateDatabase("NewDB.mdb", _ 
 dbLangGeneral) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 With dbsLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of each 
 ' Database object. 
 For Each prpLoop In .Properties 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 End With 
 Next dbsLoop 
 
 dbsNew.Close 
 dbsNorthwind.Close 
 wrkAcc.Close 
 
End Sub 
 
```

<br/>

Cet exemple utilise **CreateDatabase** pour créer un objet **Database** chiffré.

```vb
    Sub CreateDatabaseX() 
     
     Dim wrkDefault As Workspace 
     Dim dbsNew As DATABASE 
     Dim prpLoop As Property 
     
     ' Get default Workspace. 
     Set wrkDefault = DBEngine.Workspaces(0) 
     
     ' Make sure there isn't already a file with the name of 
     ' the new database. 
     If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
     ' Create a new encrypted database with the specified 
     ' collating order. 
     Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
     dbLangGeneral, dbEncrypt) 
     
     With dbsNew 
     Debug.Print "Properties of " & .Name 
     ' Enumerate the Properties collection of the new 
     ' Database object. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     End With 
     
     dbsNew.Close 
     
    End Sub
```
