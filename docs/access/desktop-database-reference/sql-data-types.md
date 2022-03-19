---
title: Types de données SQL (référence de base de données de bureau Access)
TOCTitle: SQL data types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 2e5abd817617ed3726f075be503aa240aba4a116
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627276"
---
# <a name="sql-data-types"></a>Types de données SQL

**S’applique à** : Access 2013, Office 2013

Les types de données SQL du moteur de base de données Microsoft Access comprennent 13 types de données principaux définis par le moteur de base de données Microsoft Jet et plusieurs synonymes valides reconnus pour ces types de données.

Le tableau suivant répertorie les principaux types de données. Les synonymes sont indiqués dans [Mots réservés SQL du moteur de base de données Microsoft Access](sql-reserved-words.md).

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Type de données</p></th>
<th><p>Taille</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BINARY</p></td>
<td><p>1 octet par caractère</p></td>
<td><p>Tout type de données peut être stocké dans un champ de ce type. Aucune traduction des données (par exemple, en texte) n’est effectuée. La manière dont les données sont entrées dans un champ binaire détermine la façon dont elles s’affichent en tant que sortie.</p></td>
</tr>
<tr class="even">
<td><p>BIT</p></td>
<td><p>1 octet</p></td>
<td><p>Valeurs Oui et Non, et champs contenant uniquement l’une des deux valeurs.</p></td>
</tr>
<tr class="odd">
<td><p>TINYINT</p></td>
<td><p>1 octet</p></td>
<td><p>Valeur entière comprise entre 0 et 255.</p></td>
</tr>
<tr class="even">
<td><p>MONEY</p></td>
<td><p>8 octets</p></td>
<td><p>Entier mis à l’échelle dont la valeur est comprise entre-922 337 203 685 477,5808 et 922 337 203 685 477,5807.</p></td>
</tr>
<tr class="odd">
<td><p>DATETIME (voir DOUBLE)</p></td>
<td><p>8 octets</p></td>
<td><p>Valeur de date ou d’heure comprise entre les années 100 et 9999.</p></td>
</tr>
<tr class="even">
<td><p>UNIQUEIDENTIFIER</p></td>
<td><p>128 bits</p></td>
<td><p>Numéro d’identification unique utilisé avec des appels de procédure distante.</p></td>
</tr>
<tr class="odd">
<td><p>REAL</p></td>
<td><p>4 octets</p></td>
<td><p>Valeur à virgule flottante simple précision avec une plage de -3,402823E38 à -1,401298E-45 pour les valeurs négatives, de 1,401298E-45 à 3,402823E38 pour les valeurs positives, et 0.</p></td>
</tr>
<tr class="even">
<td><p>FLOAT</p></td>
<td><p>8 octets</p></td>
<td><p>Une valeur à virgule flottante double précision avec une plage de -1,79769313486232E308 à -4,94065645841247E-324 pour les valeurs négatives, de 4,94065645841247E-324 à 1,79769313486232E308 pour les valeurs positives, et 0.</p></td>
</tr>
<tr class="odd">
<td><p>SMALLINT</p></td>
<td><p>2 octets</p></td>
<td><p>Entier court compris entre -32 768 et 32 767.</p></td>
</tr>
<tr class="even">
<td><p>INTEGER</p></td>
<td><p>4 octets</p></td>
<td><p>Entier long compris entre -2 147 483 648 et 2 147 483 647.</p></td>
</tr>
<tr class="odd">
<td><p>DECIMAL</p></td>
<td><p>17 octets</p></td>
<td><p>Type de données numériques exactes qui contient des valeurs comprises entre 1 028-1 et -1 028-1. Vous pouvez définir la précision (1-28) et l’échelle (0-précision définie). La précision et l’échelle par défaut sont respectivement de 18 et 0.</p></td>
</tr>
<tr class="even">
<td><p>TEXT</p></td>
<td><p>2 octets par caractère (voir Remarques)</p></td>
<td><p>Zéro à un maximum de 2,14 Go.</p></td>
</tr>
<tr class="odd">
<td><p>IMAGE</p></td>
<td><p>Si nécessaire</p></td>
<td><p>Zéro à un maximum de 2,14 Go. Utilisé pour les objets OLE.</p></td>
</tr>
<tr class="even">
<td><p>CHARACTER</p></td>
<td><p>2 octets par caractère (voir Remarque)</p></td>
<td><p>Jusqu’à 255 caractères.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> - La valeur de départ et l’incrément peuvent être modifiés à l’aide un [instruction TABLE modifier](alter-table-statement-microsoft-access-sql.md). Nouvelles lignes insérées dans la table comportent des valeurs basées sur la nouvelle valeur de départ et les valeurs incrément, qui sont générées automatiquement pour la colonne. Si la nouvelle valeur de départ et l’incrément pouvant rendement valeurs qui correspondent aux valeurs générées basé sur la valeur de départ et l’incrément précédente, les doublons seront générées. Si la colonne est une clé primaire, puis en insérant nouvelles lignes peut entraîner des erreurs lorsque les valeurs en double sont générés.
> - Pour rechercher la dernière valeur que vous avez utilisée pour une colonne incrément automatique, vous pouvez utiliser l’instruction suivante : sélectionnez @@IDENTITY. Vous ne pouvez pas spécifier un nom de tableau. La valeur renvoyée est à partir de la dernière table contenant une colonne incrément automatique qui a été mis à jour.
