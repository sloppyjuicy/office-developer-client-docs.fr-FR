---
title: Recordset2.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: 9bec543e-7f59-ea59-dc79-41d0e08b5ab6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198080(v=office.15)
ms:contentKeyID: 48546583
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052880
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7d35f4acb97871f9d7499b67817c6c88ae56f441
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871898"
---
# <a name="recordset2type-property-dao"></a>Recordset2.Type Property (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type de données **Integer** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Type

*expression* Variable qui représente un objet **Recordset2** .

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

