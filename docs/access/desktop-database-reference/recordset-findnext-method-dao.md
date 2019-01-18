---
title: Méthode Recordset.FindNext (DAO)
TOCTitle: FindNext Method
ms:assetid: 5457dfc8-e561-5624-74d0-34278ba2e7cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194099(v=office.15)
ms:contentKeyID: 48544893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a9ef8f1714244b02ed5423a38cf3fb8fa328ec1e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699267"
---
# <a name="recordsetfindnext-method-dao"></a>Méthode Recordset.FindNext (DAO)

**S’applique à**: Access 2013, Office 2013

Recherche l’enregistrement suivant dans un objet **[Recordset](recordset-object-dao.md)** de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés et en fait l’enregistrement actif (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . FindNext (***critères***)

*expression* Variable qui représente un objet **Recordset** .

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Requis/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Criteria</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Chaîne</strong></p></td>
<td><p>Données de type String utilisées pour localiser l'enregistrement. S'apparente à la clause WHERE d'une instruction SQL sans toutefois le mot WHERE.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Si vous souhaitez inclure tous les enregistrements dans votre recherche, et non uniquement ceux qui remplissent une condition particulière, utilisez les méthodes **Move** pour passer d'un enregistrement à un autre. Pour localiser un enregistrement dans un **Recordset** de type table, utilisez la méthode **Seek**.

Si un enregistrement correspondant aux critères n'est pas localisé, le pointeur d'enregistrement actif est inconnu et la propriété **NoMatch** est définie sur **True**. Si le recordset contient plusieurs enregistrements correspondant aux critères, **FindFirst** localise la première occurrence, **FindNext** localise l'occurrence suivante, et ainsi de suite.

Chacune des méthodes **Find** commence sa recherche à partir de l'emplacement et dans le sens spécifiés dans le tableau suivant.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Méthode Find</p></th>
<th><p>Point de départ de la recherche</p></th>
<th><p>Sens de la recherche</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>FindFirst</strong></p></td>
<td><p>Début du jeu d'enregistrements</p></td>
<td><p>Fin du jeu d'enregistrements</p></td>
</tr>
<tr class="even">
<td><p><strong>FindLast</strong></p></td>
<td><p>Fin du jeu d'enregistrements</p></td>
<td><p>Début du jeu d'enregistrements</p></td>
</tr>
<tr class="odd">
<td><p><strong>FindNext</strong></p></td>
<td><p>Enregistrement actif</p></td>
<td><p>Fin du jeu d'enregistrements</p></td>
</tr>
<tr class="even">
<td><p><strong>FindPrevious</strong></p></td>
<td><p>Enregistrement actif</p></td>
<td><p>Début du jeu d'enregistrements</p></td>
</tr>
</tbody>
</table>


L'utilisation de l'une des méthodes **Find** n'équivaut pas à utiliser une méthode **Move**, qui ne fait que rendre actif l'enregistrement initial, final, suivant ou précédent sans spécifier de condition. Vous pouvez faire suivre une opération Find d'une opération Move.

Vérifiez toujours la valeur de la propriété **NoMatch** pour déterminer si l'opération Find a réussi. Si la recherche aboutit, **NoMatch** a la valeur **False**. Si elle échoue, **NoMatch** a la valeur **True** et l'enregistrement actif n'est pas défini. Dans ce cas, vous devez positionner le pointeur d'enregistrement actif sur un enregistrement valide.

L'utilisation des méthodes **Find** avec les recordsets ODBC connectés au moteur de base de données Microsoft Access peut s'avérer inefficace. Il se peut que la reformulation de vos critères pour localiser un enregistrement spécifique soit plus rapide, surtout si vous travaillez avec des recordsets volumineux.

Dans un espace de travail ODBCDirect, les méthodes **Find** et **Seek** ne sont disponibles pour aucun objet **Recordset**, quel qu'en soit le type, car l'exécution d'une méthode **Find** ou **Seek** via une connexion ODBC n'est pas très efficace sur un réseau. Au lieu de cela, vous devez concevoir la requête (c'est-à-dire, en utilisant l’argument source de la méthode **OpenRecordset** ) avec une clause WHERE appropriée qui limite les enregistrements renvoyés à ceux qui répondent aux critères vous utiliseriez autrement dans une **recherche** ou Méthode **Seek** .

Lorsque vous travaillez avec des bases de données ODBC connectées au moteur de base de données Microsoft Access et des objets de type feuille de réponse dynamique volumineux, il est possible que vous notiez une certaine lenteur d'exécution lorsque vous utilisez la méthode **Find** ou la propriété **Sort** ou **Filter**. Pour améliorer les performances, utilisez des requêtes SQL avec des clauses personnalisées ORDER BY ou WHERE, des requêtes Paramètre ou des objets **QueryDef** qui extraient des enregistrements indexés spécifiques.

Il est recommandé d'utiliser le format de date des États-Unis (mois-jour-année) lorsque vous effectuez des recherches dans des champs contenant des dates, même si vous n'utilisez pas la version américaine du moteur de base de données Microsoft Access ; à défaut, les données risquent d'être introuvables. Vous pouvez utiliser la fonction **Format** de Visual Basic pour convertir la date. Par exemple :

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

Si l’argument critères se compose d’une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strSQL = « prix \> » & lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez de Appelez la méthode. En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.

> [!NOTE]
> - Pour optimiser les performances, les *critères* doivent être dans un le formulaire «*champ* = *valeur*» où *champ* représente un champ indexé dans la table de base sous-jacente, ou «*champ* LIKE *préfixe » où *le champ* est*un les champs indexés dans la table de base sous-jacente et le *préfixe* est une chaîne de recherche de préfixe (par exemple, « ART * »).
> 
> - En règle générale, pour des types de recherches équivalents, la méthode **Seek** offre de meilleures performances que la méthode **Find**. Cela suppose que les objets **Recordset** de type table peuvent à eux seuls répondre à vos besoins.


## <a name="example"></a>Exemple

L'exemple suivant montre comment utiliser les méthodes FindFirst et FindNext pour rechercher un enregistrement dans un Recordset.

**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```
