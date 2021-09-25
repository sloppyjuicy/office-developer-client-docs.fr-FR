---
title: ReadyState, propriété (RDS)
TOCTitle: ReadyState property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e1dab8baeeef547c93e8e3ced89ed3fc24ab97f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562404"
---
# <a name="readystate-property-rds"></a>ReadyState, propriété (RDS)

**S’applique à** : Access 2013, Office 2013

Indique la progression d’un [DataControl](datacontrol-object-rds.md) lorsqu’il récupère des données dans son objet [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie l'une des valeurs suivantes.

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
<td><p><strong>adcReadyStateLoaded</strong></p></td>
<td><p>La requête est encore en cours d'exécution et aucune ligne n'a été extraite. L'objet <strong>Recordset</strong> de <strong>DataControl</strong> n'est pas utilisable.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcReadyStateInteractive</strong></p></td>
<td><p>Le premier jeu de lignes récupéré par la requête actuelle a été stocké dans le <strong>Recordset</strong> de l'objet <strong>DataControl</strong> et peut être utilisé. Les lignes restantes sont encore en cours d'extraction.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcReadyStateComplete</strong></p></td>
<td><p>Toutes les lignes extraites par la requête en cours ont été stockées dans le <strong>Recordset</strong> de l'objet <strong>DataControl</strong> et peuvent être utilisées. Cet état est aussi défini lorsque l'opération a été interrompue en raison d'une erreur ou de la non-initialisation de l'objet <strong>Recordset</strong>.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!REMARQUE] Chaque fichier exécutable côté client utilisant ces constantes doit fournir les déclarations correspondantes. Vous pouvez couper et coller les déclarations de constante dont vous avez besoin dans le fichier Adcvbs.inc placé dans le dossier C:\Program Files\Common Files\System\MSADC.

## <a name="remarks"></a>Remarques

Utilisez l’événement [onreadystatechange](onreadystatechange-event-rds.md) pour surveiller les modifications de la propriété **ReadyState** lors d’une requête asynchrone. C’est plus efficace que de vérifier régulièrement la valeur de la propriété.

Si une erreur se produit au cours d’une opération asynchrone, la propriété [](value-property-ado.md) **ReadyState** passe à **adcReadyStateComplete**, la propriété [State](state-property-ado.md) passe d’adStateExecuting à **adStateClosed** et la propriété Valeur de l’objet **Recordset** reste *Nothing*. 

