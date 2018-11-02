---
title: Propriété Recordset.Type (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 85e518dc5d13a6e8e70c449fb35158395b7a13aa
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920724"
---
# <a name="recordsettype-property-dao"></a>Propriété Recordset.Type (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type de données **Integer** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Type

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

Pour un objet **Recordset**, les paramètres et valeurs de retour possibles sont les suivants.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Type d'objet Recordset</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbOpenTable</strong></p></td>
<td><p>Table (espaces de travail Microsoft Access uniquement)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbOpenDynamic</strong></p></td>
<td><p>Dynamique (espaces de travail ODBCDirect uniquement)</p>

> [!NOTE]
> <P>[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>dbOpenDynaset</strong></p></td>
<td><p>Feuille de réponse dynamique</p></td>
</tr>
<tr class="even">
<td><p><strong>dbOpenSnapshot</strong></p></td>
<td><p>Instantané</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbOpenForwardOnly</strong></p></td>
<td><p>Avant uniquement</p></td>
</tr>
</tbody>
</table>

