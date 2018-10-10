---
title: TableDef.ReplicaFilter Property (DAO)
TOCTitle: ReplicaFilter Property
ms:assetid: f44273de-2b6a-750f-cb7c-12c3ac2da503
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836681(v=office.15)
ms:contentKeyID: 48548683
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055548
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5104aa452dfc8bc73c378c30a454f676d455c9f1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471847"
---
# <a name="tabledefreplicafilter-property-dao"></a>TableDef.ReplicaFilter Property (DAO)


**S’applique à**: Access 2013 | Office 2013

Définit ou renvoie une valeur sur un objet **[TableDef](tabledef-object-dao.md)** au sein d'un réplica partiel qui indique le sous-ensemble d'enregistrements répliqué vers cette table à partir d'un réplica complet. (Espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . ReplicaFilter

*expression* Variable qui représente un objet **TableDef** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est un type **String** ou **Boolean** spécifiant le sous-ensemble d'enregistrements qui est répliqué, comme indiqué dans le tableau suivant :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Chaîne de caractères</p></td>
<td><p>Critère auquel un enregistrement de la table du réplica partiel doit satisfaire afin d'être répliqué à partir du réplica complet.</p></td>
</tr>
<tr class="even">
<td><p><strong>True</strong></p></td>
<td><p>Réplique tous les enregistrements</p></td>
</tr>
<tr class="odd">
<td><p><strong>False</strong></p></td>
<td><p>(Par défaut) Ne réplique aucun enregistrement.</p></td>
</tr>
</tbody>
</table>


Cette propriété est similaire à une clause SQL WHERE (sans le mot WHERE) à cette différence que vous ne pouvez pas spécifier de sous-requêtes, de fonctions d'agrégation (p.ex. **Count**) ni de fonctions définies par l'utilisateur dans les critères.

La synchronisation des données n'est possible qu'entre un réplica complet et un réplica partiel. Vous ne pouvez pas synchroniser des données entre deux réplicas partiels. En outre, avec la réplication partielle, vous pouvez définir des restrictions quant aux enregistrements à répliquer mais vous ne pouvez pas indiquer quels champs sont répliqués.

En général vous redéfinissez un filtre de réplica lorsque vous souhaitez répliquer un autre jeu d'enregistrements. Par exemple, lorsqu'un représentant commercial reprend provisoirement le territoire de vente d'un autre représentant, l'application de base de données peut répliquer temporairement les données pour les deux régions puis revenir au filtre précédent. Dans ce scénario, l'application redéfinit la propriété **ReplicaFilter** puis remplit à nouveau le réplica partiel.

Si votre application modifie les filtres de réplica, procédez comme suit :

1.  Appelez la méthode **[Synchronize](database-synchronize-method-dao.md)** pour synchroniser votre réplica complet avec le réplica partiel dans lequel les filtres sont modifiés.

2.  Utilisez la propriété **ReplicaFilter** pour apporter les modifications requises au filtre de réplica.

3.  Appelez la méthode **[PopulatePartial](database-populatepartial-method-dao.md)** pour supprimer tous les enregistrement du réplica partiel et transférer tous les enregistrements du réplica complet correspondant aux nouveaux critères de filtre de réplica.

Pour supprimer un filtre, affectez à la propriété **ReplicaFilter** la valeur **False**. Si vous supprimez tous les filtres et que vous appelez la méthode **PopulatePartial**, aucun enregistrement n'apparaîtra dans les tables répliquées du réplica partiel.


> [!NOTE]
> <P>[!REMARQUE] Si un filtre de réplica a été modifié et que la méthode <STRONG>Synchronize</STRONG> est exécutée sans avoir préalablement appelé la méthode <STRONG>PopulatePartial</STRONG>, une erreur piégeable se produit.</P>



## <a name="example"></a>Exemple

L'exemple suivant utilise la propriété **ReplicaFilter** pour répliquer uniquement les enregistrements clients de Californie.

```vb 
Sub ReplicaFilterX() 
 
 ' This example assumes the current open database 
 ' is the replica. 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 Set dbsTemp = OpenDatabase("Northwind.mdb") 
 Set tdfCustomers = dbsTemp.TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 dbsTemp.Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 dbsTemp.PopulatePartial "C:\SALES\FY96.MDB" 
 
 ' Now remove the replica filter (for example purposes 
 ' only). 
 tdfCustomers.ReplicaFilter = False 
 ' Repopulate the database. 
 dbsTemp.PopulatePartial "C:\SALES\DATA96.MDB" 
 
End Sub 
 
```

