---
title: ExecuteOptions, propriété (RDS)
TOCTitle: ExecuteOptions Property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 641e7942f5336f230d396db7e06b9d0601645cb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469556"
---
# <a name="executeoptions-property-rds"></a>ExecuteOptions, propriété (RDS)


**S’applique à**: Access 2013 | Office 2013

Indique si l'exécution asynchrone est activée.

## <a name="settings-and-return-values"></a>Paramètres et valeurs renvoyées

Définit ou renvoie l'une des valeurs suivantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>valeur adcExecSync</strong></p></td>
<td><p>Exécute l’actualisation suivante du <a href="recordset-object-ado.md">Recordset</a> de façon asynchrone.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcExecAsync</strong></p></td>
<td><p>Valeur par défaut. Exécute l'actualisation suivante du <strong>Recordset</strong> de façon asynchrone.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>[!REMARQUE] Chaque fichier exécutable côté client utilisant ces constantes doit fournir les déclarations correspondantes. Vous pouvez couper et coller les déclarations de constante dont vous avez besoin dans le fichier Adcvbs.inc placé dans le dossier C:\Program Files\Common Files\System\MSADC.</P>



## <a name="remarks"></a>Remarques

Si **ExecuteOptions** est défini sur **adcExecAsync**, l'appel suivant de **Refresh** est exécuté de façon asynchrone sur le [Recordset](datacontrol-object-rds.md) de l'objet **RDS.DataControl**.

Si vous essayez d'appeler [Reset](reset-method-rds.md),[Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md) ou [Recordset](recordset-sourcerecordset-properties-rds.md) pendant l'exécution d'une autre opération asynchrone susceptible de modifier le [Recordset](datacontrol-object-rds.md) de l'objet **RDS.DataControl**, une erreur se produit.

S’il se produit une erreur pendant une opération asynchrone, la valeur [ReadyState](readystate-property-rds.md) de l’objet **RDS.DataControl** (**adcReadyStateLoaded**) est remplacée par **adcReadyStateComplete** et la valeur de la propriété **Recordset** reste la même : *Nothing*.

