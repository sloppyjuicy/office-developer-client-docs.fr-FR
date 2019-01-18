---
title: Données persistantes (référence de base de données du bureau Access)
TOCTitle: Persisting data
ms:assetid: cb8a32f7-2cdc-26ed-c6d4-dd93c1ac37ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250010(v=office.15)
ms:contentKeyID: 48547715
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f5788216a20e62cfc39fd2081f4f672bc4f9b808
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713960"
---
# <a name="persisting-data"></a>Persistance des données


**S’applique à**: Access 2013, Office 2013

L'informatique nomade, notamment par l'utilisation d'ordinateurs portables, a généré un besoin d'applications capables d'être exécutées à la fois de manière autonome et en réseau. ADO prend désormais en charge ce phénomène en donnant la possibilité au développeur d'enregistrer un **jeu d'enregistrements** de curseur client sur un disque pour le recharger ultérieurement.

Divers scénarios requièrent l'utilisation de cette fonctionnalité, notamment :

- **Déplacements :** lorsque vous vous déplacez avec l'application, il est crucial de pouvoir effectuer des modifications et d'ajouter de nouveaux enregistrements qui peuvent ensuite être soumis à la base de données et validés.

- **Tables de choix rarement mises à jour :** dans une application, les tables sont souvent utilisées comme des tables de choix  par exemple, les tables de taxes. Elles sont rarement mises à jour et en lecture seule. Au lieu de relire ces données à partir du serveur à chaque démarrage de l'application, cette dernière peut simplement les charger à partir d'un **jeu d'enregistrements** conservé localement.

Dans ADO, pour enregistrer et charger des **jeux d'enregistrements**, utilisez les méthodes **Recordset.Save** et **Recordset.Open(,,,,adCmdFile)** sur l'objet **Recordset** ADO.

Vous pouvez utiliser la méthode **Recordset** **Save** pour stocker votre **jeu d'enregistrements** ADO dans un fichier sur un lecteur. (Vous pouvez également enregistrer un **jeu d'enregistrements** sur un objet **Stream** ADO. Les objets **Stream** sont abordés plus loin dans ce guide.) Vous pouvez ensuite utiliser la méthode **Open** pour rouvrir le **jeu d'enregistrements** lorsque vous voulez l'utiliser. Par défaut, ADO enregistre le **jeu d'enregistrements** au format propriétaire Microsoft Advanced Data TableGram (ADTG). Ce format binaire est spécifié à l'aide de la valeur **adPersistADTG** **PersistFormatEnum**. Vous pouvez également choisir d'enregistrer votre **jeu d'enregistrements** au format XML en utilisant **adPersistXML**. Pour en savoir plus sur l'enregistrement des jeux d'enregistrements au format XML, reportez-vous à la rubrique [Enregistrements persistants au format XML](persisting-records-in-xml-format.md).

La syntaxe de la méthode **Save** est la suivante :

`recordset.Save Destination, PersistFormat`

La première fois que vous enregistrez le **jeu d’enregistrements**, il n’est pas nécessaire d’indiquer une *destination*. Si vous oubliez la *destination*, un nouveau fichier est créé et nommé selon la valeur de la propriété [Source](source-property-ado-recordset.md) du **jeu d’enregistrements**.

Ne spécifiez pas de *destination* lors des prochaines invocations de **Save** après le premier enregistrement. Dans le cas contraire, une erreur d'exploitation survient. Si vous invoquez **Save** plus tard avec une nouvelle *destination*, le **jeu d'enregistrements** est enregistré dans le nouvel emplacement. Toutefois, cet emplacement et l'emplacement d'origine restent tous les deux ouverts.

La méthode **Save** ne ferme pas le **jeu d'enregistrements** ni la *destination*. Vous pouvez donc continuer à utiliser le **jeu d'enregistrements** et sauvegarder vos modifications les plus récentes. La *destination* reste ouverte jusqu'à ce que le **jeu d'enregistrements** soit fermé. Pendant ce temps, les autres applications peuvent lire mais pas écrire dans la *destination*.

Pour des raisons de sécurité, la méthode **Save** autorise uniquement l'utilisation des paramètres de sécurité faible et personnalisée d'un script exécuté par Microsoft Internet Explorer. Pour une explication plus détaillée des problèmes de sécurité, reportez-vous à l'article (en anglais) « ADO and RDS Security Issues in Microsoft Internet Explorer » dans la rubrique Microsoft Data Access Technical Articles du site MSDN.

Si une méthode **Save** est invoquée alors qu'une opération asynchrone de mise à jour, d'exécution ou d'extraction d'un **jeu d'enregistrements** est en cours, la méthode **Save** attend la fin de l'opération asynchrone.

La sauvegarde des enregistrements s'effectue à partir de la première ligne du **jeu d'enregistrements**. À la fin de la méthode **Save**, la position de ligne active est placée sur la première ligne du **jeu d'enregistrements**.

Pour obtenir de meilleurs résultats, affectez à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient** avec la méthode **Save**. Si votre fournisseur ne prend pas en charge toutes les fonctionnalités nécessaires à l'enregistrement des objets **Recordset**, le service de curseur les fournira.

Lorsqu'un objet **Recordset** est conservé avec la propriété **CursorLocation** affectée de la valeur **adUseServer**, les fonctionnalités de mise à jour de l'objet **Recordset** sont limitées. En règle générale, seules les mises à jour de la table unique, des insertions et suppressions sont autorisées (dépendantes de la fonctionnalité du fournisseur). La méthode [Resync](resync-method-ado.md) n'est pas non plus disponible avec une telle configuration.

Étant donné que le paramètre *Destination* accepte tout objet qui prend en charge l’interface OLE DB **IStream** , vous pouvez enregistrer un **objet Recordset** directement dans l’objet ASP **Response** .

Dans l'exemple suivant, les méthodes **Save** et **Open** sont utilisées pour conserver un **jeu d'enregistrements** et le rouvrir plus tard :

```vb 
 
'BeginPersist 
 conn.ConnectionString = _ 
 "Provider='SQLOLEDB';Data Source='MySqlServer';" _ 
 & "Integrated Security='SSPI';Initial Catalog='pubs'" 
 conn.Open 
 
 conn.Execute "create table testtable (dbkey int " & _ 
 "primary key, field1 char(10))" 
 conn.Execute "insert into testtable values (1, 'string1')" 
 
 Set rst.ActiveConnection = conn 
 rst.CursorLocation = adUseClient 
 
 rst.Open "select * from testtable", conn, adOpenStatic, _ 
 adLockBatchOptimistic 
 
 'Change the row on the client 
 rst!field1 = "NewValue" 
 
 'Save to a file--the .dat extension is an example; choose 
 'your own extension. The changes will be saved in the file 
 'as well as the original data. 
 MyFile = Dir("c:\temp\temptbl.dat") 
 If MyFile <> "" Then 
 Kill "c:\temp\temptbl.dat" 
 End If 
 
 rst.Save "c:\temp\temptbl.dat", adPersistADTG 
 rst.Close 
 Set rst = Nothing 
 
 'Now reload the data from the file 
 Set rst = New ADODB.Recordset 
 rst.Open "c:\temp\temptbl.dat", , adOpenStatic, _ 
 adLockBatchOptimistic, adCmdFile 
 
 Debug.Print "After Loading the file from disk" 
 Debug.Print " Current Edited Value: " & rst!field1.Value 
 Debug.Print " Value Before Editing: " & rst!field1.OriginalValue 
 
 'Note that you can reconnect to a connection and 
 'submit the changes to the data source 
 Set rst.ActiveConnection = conn 
 rst.UpdateBatch 
'EndPersist 
```

Cette section comprend les rubriques suivantes :

- [En savoir plus sur la persistance des objets Recordset](more-about-recordset-persistence.md)

- [Conservation des jeux d’enregistrements hiérarchiques et filtrés](persisting-filtered-and-hierarchical-recordsets.md)

- [Persisting Records in XML Format (ADO)](persisting-records-in-xml-format.md)
