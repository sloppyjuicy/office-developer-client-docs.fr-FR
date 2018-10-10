---
title: ReadyState, propriété (RDS)
TOCTitle: ReadyState Property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 804a98a6fa7c93617a5b6e165a2a012969c66913
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471177"
---
# <a name="readystate-property-rds"></a>ReadyState, propriété (RDS)


**S’applique à**: Access 2013 | Office 2013

Indique la progression d'un [DataControl](datacontrol-object-rds.md) lorsqu'il récupère des données dans son objet [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs renvoyées

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
<td><p><strong>(adcReadyStateLoaded)</strong></p></td>
<td><p>La requête est encore en cours d'exécution et aucune ligne n'a été extraite. L'objet <strong>Recordset</strong> de <strong>DataControl</strong> n'est pas utilisable.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcReadyStateInteractive</strong></p></td>
<td><p>Le premier jeu de lignes récupéré par la requête actuelle a été stocké dans le <strong>Recordset</strong> de l'objet <strong>DataControl</strong> et peut être utilisé. Les lignes restantes sont encore en cours d'extraction.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcReadyStateComplete</strong></p></td>
<td><p>Toutes les lignes extraites par la requête en cours ont été stockées dans le <strong>Recordset</strong> de l'objet <strong>DataControl</strong> et peuvent être utilisées.
 Cet état est aussi défini lorsque l'opération a été interrompue en raison d'une erreur ou de la non-initialisation de l'objet <strong>Recordset</strong>.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>[!REMARQUE] Chaque fichier exécutable côté client utilisant ces constantes doit fournir les déclarations correspondantes. Vous pouvez couper et coller les déclarations de constante dont vous avez besoin dans le fichier Adcvbs.inc placé dans le dossier C:\Program Files\Common Files\System\MSADC.</P>



## <a name="remarks"></a>Remarques

Utilisez l'événement [onreadystatechange](onreadystatechange-event-rds.md) pour surveiller les modifications de la propriété **ReadyState** lors d'une requête asynchrone. C'est plus efficace que de vérifier régulièrement la valeur de la propriété.

Si une erreur se produit pendant une opération asynchrone, la propriété **ReadyState** devient **adcReadyStateComplete**, la propriété [State](state-property-ado.md) passe de **adStateExecuting** à **adStateClosed**et le **jeu d’enregistrements** [valeur de](value-property-ado.md) propriété de l’objet reste *Nothing*.

