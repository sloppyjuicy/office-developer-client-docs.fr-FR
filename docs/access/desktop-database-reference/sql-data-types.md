---
title: Types de données SQL (référence de base de données du bureau Access)
TOCTitle: SQL Data Types
ms:assetid: 4fc2dc8c-7825-8fbb-ff91-a0f39ef90115
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193793(v=office.15)
ms:contentKeyID: 48544783
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277590
f1_categories:
- Office.Version=v15
ms.openlocfilehash: cfaecd26ebd3f747a0e2db2ec530c151928fec74
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936909"
---
# <a name="sql-data-types"></a>Types de données SQL


**S’applique à**: Access 2013, Office 2013

Les types de données SQL du moteur de base de données Microsoft Access se composent de 13 types de données principaux définis par le moteur de base de données Microsoft Jet et plusieurs synonymes valides reconnus pour ces types de données.

Le tableau suivant répertorie les principaux types de données. Les synonymes sont indiqués dans [Mots réservés SQL du moteur de base de données Microsoft Access](sql-reserved-words.md).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td><p>1 octet par caractère</p></td>
<td><p>N'importe quel type de données peut être stocké dans un champ de ce type. Aucune conversion des données (par exemple, en texte) n'est effectuée. La manière dont les données sont entrées dans un champ binaire détermine comment elles apparaîtront une fois produites.</p></td>
</tr>
<tr class="even">
<td><p>BIT</p></td>
<td><p>1 octet</p></td>
<td><p>Les valeurs Oui et Non et les champs qui contiennent une de ces deux valeurs.</p></td>
</tr>
<tr class="odd">
<td><p>TINYINT</p></td>
<td><p>1 octet</p></td>
<td><p>Une valeur entière entre 0 et 255.</p></td>
</tr>
<tr class="even">
<td><p>MONEY</p></td>
<td><p>8 octets</p></td>
<td><p>Un entier décalé entre – 922 337 203 685 477,5808 et 922 337 203 685 477,5807.</p></td>
</tr>
<tr class="odd">
<td><p>DATETIME (voir DOUBLE)</p></td>
<td><p>8 octets</p></td>
<td><p>Valeur de date ou d'heure entre les années 100 et 9999.</p></td>
</tr>
<tr class="even">
<td><p>UNIQUEIDENTIFIER</p></td>
<td><p>128 bits</p></td>
<td><p>Numéro d'identification unique utilisé avec des appels de procédure distante.</p></td>
</tr>
<tr class="odd">
<td><p>REAL</p></td>
<td><p>4 octets</p></td>
<td><p>Valeur à virgule flottante (simple précision) comprise entre – 3,402823E38 et – 1,401298E-45 pour les valeurs négatives et entre 1,401298E-45 et 3,402823E38 pour les valeurs positives et 0.</p></td>
</tr>
<tr class="even">
<td><p>FLOAT</p></td>
<td><p>8 octets</p></td>
<td><p>Valeur à virgule flottante (double précision) comprise entre – 1,79769313486232E308 et – 4,94065645841247E-324 pour les valeurs négatives et entre 4,94065645841247E-324 et 1,79769313486232E308 pour les valeurs positives et 0.</p></td>
</tr>
<tr class="odd">
<td><p>SMALLINT</p></td>
<td><p>2 octets</p></td>
<td><p>Entier court entre – 32 768 et 32 767. (Voir Remarques)</p></td>
</tr>
<tr class="even">
<td><p>INTEGER</p></td>
<td><p>4 octets</p></td>
<td><p>Entier long entre – 2 147 483 648 et 2 147 483 647. (Voir Remarques)</p></td>
</tr>
<tr class="odd">
<td><p>DECIMAL</p></td>
<td><p>17 octets</p></td>
<td><p>Type de données numériques exactes qui contient des valeurs entre 1028 - 1 et - 1028 - 1. Vous pouvez définir la précision (1 - 28) et l'échelle (0 - précision définie). La précision et l'échelle par défaut sont respectivement 18 et 0.</p></td>
</tr>
<tr class="even">
<td><p>TEXT</p></td>
<td><p>2 octets par caractère (voir Remarques)</p></td>
<td><p>Entre 0 et 2,14 gigaoctets maximum.</p></td>
</tr>
<tr class="odd">
<td><p>IMAGE</p></td>
<td><p>En fonction des besoins</p></td>
<td><p>Entre 0 et 2,14 gigaoctets maximum. Utilisé pour les objets OLE.</p></td>
</tr>
<tr class="even">
<td><p>CHARACTER</p></td>
<td><p>2 octets par caractère (voir Remarques)</p></td>
<td><p>Entre zéro et 255 caractères.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <UL>
> <LI>
> <P>La valeur de départ et la valeur incrémentielle peuvent être modifiées à l'aide d'une <A href="alter-table-statement-microsoft-access-sql.md">instruction ALTER TABLE</A>. Les nouvelles lignes insérées dans la table comportent des valeurs basées sur la nouvelle valeur de départ et la nouvelle valeur incrémentielle qui sont automatiquement générées pour la colonne. Si ces nouvelles valeurs peuvent produire des valeurs qui correspondent à celles générées à partir de la valeur de départ et de la valeur incrémentielle d'origine, des valeurs en double sont générées. Si la colonne est une clé primaire, l'insertion de nouvelles lignes peut produire des erreurs lorsque des valeurs en double sont générées.</P>
> <LI>
> <P>Pour rechercher la dernière valeur qui a été utilisée pour une colonne incrémentée automatiquement, vous pouvez utiliser l'instruction suivante : SELECT @@IDENTITY. En revanche, vous ne pouvez pas spécifier le nom d'une table. La valeur renvoyée provient de la dernière table contenant une colonne incrémentée automatiquement qui a été dupliquée.</P></LI></UL>


