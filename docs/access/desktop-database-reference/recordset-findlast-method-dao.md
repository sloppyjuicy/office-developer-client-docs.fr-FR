---
title: Recordset.FindLast, méthode (DAO)
TOCTitle: FindLast Method
ms:assetid: 65236519-3474-a760-99bc-2e8f6bfeee7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195128(v=office.15)
ms:contentKeyID: 48545311
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b5452d0de206080b644203c615b40de0bf7b06fb
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375068"
---
# <a name="recordsetfindlast-method-dao"></a>Recordset.FindLast, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Recherche le dernier enregistrement dans un objet **[Recordset](recordset-object-dao.md)** de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés, et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*.* FindLast(***Criteria***)

*expression* Variable représentant un objet **Recordset**.

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
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Critères</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Données de type String utilisées pour localiser l'enregistrement. S'apparente à la clause WHERE d'une instruction SQL sans toutefois le mot WHERE.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Remarques

Si vous souhaitez inclure tous les enregistrements dans votre recherche, et non uniquement ceux qui remplissent une condition particulière, utilisez les méthodes **Move** pour passer d’un enregistrement à un autre. Pour localiser un enregistrement dans un **Recordset** de type table, utilisez la méthode **Seek**.

Si un enregistrement correspondant aux critères n’est pas localisé, le pointeur d’enregistrement actif est inconnu et la propriété **NoMatch** est définie sur **True**. Si le recordset contient plusieurs enregistrements correspondant aux critères, **FindFirst** localise la première occurrence, **FindNext** localise l’occurrence suivante, et ainsi de suite.

Chacune des méthodes **Find** commence sa recherche à partir de l’emplacement et dans le sens spécifiés dans le tableau suivant.

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
<td><p>Fin du jeu d’enregistrements</p></td>
</tr>
<tr class="even">
<td><p><strong>FindLast</strong></p></td>
<td><p>Fin du jeu d'enregistrements</p></td>
<td><p>Début du jeu d’enregistrements</p></td>
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

Lorsque vous utilisez la méthode **FindLast**, le moteur de base de données Microsoft Access remplit entièrement votre objet **Recordset** avant de lancer la recherche, si cela n'a pas déjà été fait.

L’utilisation de l’une des méthodes **Find** n’équivaut pas à utiliser une méthode **Move**, qui ne fait que rendre actif l’enregistrement initial, final, suivant ou précédent sans spécifier de condition. Vous pouvez faire suivre une opération Find d’une opération Move.

Vérifiez toujours la valeur de la propriété **NoMatch** pour déterminer si l’opération Find a réussi. Si la recherche aboutit, **NoMatch** a la valeur **False**. Si elle échoue, **NoMatch** a la valeur **True** et l’enregistrement actif n’est pas défini. Dans ce cas, vous devez positionner le pointeur d’enregistrement actif sur un enregistrement valide.

L’utilisation des méthodes **Find** avec les recordsets ODBC connectés au moteur de base de données Microsoft Access peut s’avérer inefficace. Il se peut que la reformulation de vos critères pour localiser un enregistrement spécifique soit plus rapide, surtout si vous travaillez avec des recordsets volumineux.

Lorsque vous utilisez des bases de données ODBC connectées au moteur de base de données Microsoft Access et de grands objets **Recordset** de type feuille de réponse dynamique, il se peut que l’utilisation des méthodes **Find** ou des propriétés **Sort** ou **Filter** soit lente. Pour améliorer les performances, utilisez des requêtes SQL avec des clauses ORDER BY ou WHERE personnalisées, des requêtes avec paramètres ou des objets **QueryDef** qui récupèrent des enregistrements indexés spécifiques.

Vous devez utiliser un format de date américain (mois-jour-année) lorsque vous recherchez des champs contenant des dates, même si vous n’utilisez pas la version américaine du moteur de base de données Microsoft Access. Sinon, les données risquent de ne pas être trouvées. Utilisez la fonction **Format** de Visual Basic pour convertir la date. Par exemple :

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

Si les critères sont composés d’une chaîne concaténée avec une valeur non entière, et que les paramètres système indiquent un caractère décimal non américain, comme une virgule (par exemple, strSQL = "PRICE \> " & lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous tentez d’appeler la méthode. Ceci est dû au fait que, lors de la concaténation, le nombre sera converti en chaîne à l’aide du caractère décimal par défaut de votre système, et Microsoft Access SQL accepte uniquement les caractères décimaux américains.

> [!NOTE]
> Pour des performances optimales, les *critères* doivent être au format «*champ* = *valeur*» où *champ* est un champ indexé dans la table de base sous-jacente, ou au format «*champ* LIKE *préfixe*» où *champ* est un champ indexé dans la table de base sous-jacente et *préfixe* une chaîne de recherche de préfixe (par exemple, « ART* »).
> En règle générale, pour des types de recherches équivalents, la méthode **Seek** offre de meilleures performances que la méthode **Find**. Cela suppose que les objets **Recordset** de type table peuvent à eux seuls répondre à vos besoins.
