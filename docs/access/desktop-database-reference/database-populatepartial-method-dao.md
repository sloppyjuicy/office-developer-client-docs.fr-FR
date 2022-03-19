---
title: Database.PopulatePartial method (DAO)
TOCTitle: PopulatePartial Method
ms:assetid: fa3227a2-c961-6a98-32b3-5b6e5329a21d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837034(v=office.15)
ms:contentKeyID: 48548834
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101186
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 0e2c077392d9a31967ba7f9933fe006f2bc00eed
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63629236"
---
# <a name="databasepopulatepartial-method-dao"></a>Database.PopulatePartial method (DAO)

**S’applique à** : Access 2013, Office 2013

Synchronise les modifications d'un réplica partiel avec le réplica complet, efface tous les enregistrements du réplica partiel, puis remplit à nouveau ce dernier en fonction des filtres de réplica actifs. (Bases de données du moteur de base de données Microsoft Access uniquement.)

## <a name="syntax"></a>Syntaxe

*.* PopulatePartial(***DbPathName***)

*expression* Variable qui représente un objet **Database**.

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>DbPathName</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Chemin d'accès et nom du réplica complet à partir duquel les enregistrements sont remplis.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Lorsque vous synchronisez un réplica partiel avec un réplica complet, il est possible de créer des enregistrements « orphelins » dans le réplica partiel. Par exemple, supposons que vous avez une table Customers dont **[le replicaFilter](tabledef-replicafilter-property-dao.md)** a la valeur « Region = 'CA' ». Si un utilisateur modifie la région d'un client en remplaçant CA par NY dans le réplica partiel, puis qu'une synchronisation est conduite via la méthode **[Synchronize](database-synchronize-method-dao.md)**, la modification est propagée dans le réplica complet, mais l'enregistrement contenant NY dans le réplica partiel devient orphelin, car il ne correspond plus aux critères du filtre de réplica.

Pour résoudre le problème des enregistrements orphelins, vous pouvez utiliser la méthode **PopulatePartial**. La méthode **PopulatePartial** est similaire à la méthode **Synchronize**, à ceci près qu'elle synchronise les modifications avec le réplica complet, qu'elle supprime tous les enregistrements dans le réplica partiel, puis qu'elle remplit à nouveau le réplica partiel en fonction des filtres de réplica actifs. Même si vos filtres de réplica n'ont pas changé, **PopulatePartial** efface invariablement l'ensemble des enregistrements du réplica partiel et le remplit à nouveau en fonction des filtres actifs.

En règle générale, le recours à la méthode **PopulatePartial** s'avère judicieux dans le cadre de la création d'un réplica partiel et chaque fois que les filtres de réplica sont modifiés. Si votre application modifie les filtres de réplica, il est conseillé d'exécuter la procédure suivante :

1.  Synchronisez votre réplica complet avec le réplica partiel dont les filtres sont modifiés.

2.  Utilisez les propriétés **ReplicaFilter** et **[PartialReplica](relation-partialreplica-property-dao.md)** pour apporter les modifications souhaitées au filtre de réplica.

3.  Appelez la méthode **PopulatePartial** pour supprimer tous les enregistrements du réplica partiel et transférer tous ceux du réplica complet correspondant aux nouveaux critères du filtre de réplica.

Si vous modifiez un filtre de réplica et que la méthode **Synchronize** est appelée sans que la méthode **PopulatePartial** ait été d'abord appelée, une erreur interceptable se produit.

La méthode **PopulatePartial** ne peut être appelée que sur un réplica partiel ouvert dans le cadre d'un accès exclusif. De plus, vous ne pouvez pas appeler la méthode **PopulatePartial** à partir du code s'exécutant à l'intérieur du réplica partiel proprement dit. Au lieu de cela, ouvrez le réplica partiel en mode exclusif à partir du réplica complet ou d'une autre base de données, puis appelez **PopulatePartial**.


> [!NOTE]
> [!REMARQUE] Même si **PopulatePartial** effectue une synchronisation unidirectionnelle avant d'effacer et de remplir à nouveau le réplica partiel, il est judicieux d'appeler **Synchronize** avant **PopulatePartial**. En effet, si l'appel de **Synchronize** échoue, une erreur interceptable se produit. Cette erreur peut vous être utile pour décider s'il convient ou non de poursuivre avec la méthode **PopulatePartial** (laquelle supprime tous les enregistrements du réplica partiel). Si **PopulatePartial** s'appelle elle-même et qu'une erreur se produit alors que les enregistrements sont en cours de synchronisation, les enregistrements du réplica partiel sont quand même effacés, ce qui peut ne pas correspondre au résultat souhaité.



## <a name="example"></a>Exemple

L'exemple de code suivant montre comment utiliser la méthode **PopulatePartial** après avoir modifié un filtre de réplica.

```vb 
Sub PopulatePartialX() 
 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 ' Open the partial replica in exclusive mode. 
 Set dbsTemp = OpenDatabase("F:\SALES\FY96CA.MDB", True) 
 
 With dbsTemp 
 Set tdfCustomers = .TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 .Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 
 ' Populate records from the full replica. 
 .PopulatePartial "C:\SALES\FY96.MDB" 
 
 .Close 
 End With 
 
End Sub 
 
```

