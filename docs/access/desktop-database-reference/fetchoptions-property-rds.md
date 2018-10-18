---
title: FetchOptions, propriété (RDS)
TOCTitle: FetchOptions Property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f98872c3eae47e1b657e0b16b5df5b5c46b421a5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25607017"
---
# <a name="fetchoptions-property-rds"></a>FetchOptions, propriété (RDS)


**S’applique à**: Access 2013 | Office 2013

Indique le type d'extraction asynchrone.

## <a name="setting-and-return-values"></a>Paramètre et valeur renvoyée

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
<td><p><strong>valeur adcFetchUpFront</strong></p></td>
<td><p>Tous les enregistrements du <a href="recordset-object-ado.md">Recordset</a> sont extraits avant que le contrôle ne soit renvoyé à l’application. L’objet <strong>Recordset</strong> complet est extrait avant que l’application ne puisse en faire quoi que ce soit.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcFetchBackground</strong></p></td>
<td><p>Le contrôle est rendu à l'application dès que le premier lot d'enregistrements a été extrait. La demande suivante de lecture d'un <strong>Recordset</strong> non extrait dans le premier lot est retardée jusqu'à ce que l'enregistrement concerné soit extrait ; le contrôle revient alors à l'application.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcFetchAsync</strong></p></td>
<td><p>Valeur par défaut. Le contrôle est immédiatement rendu à l’application pendant que des enregistrements sont extraits en arrière-plan. Si l’application tente de lire un enregistrement qui n’a pas encore été extrait, c’est l’enregistrement le plus proche de l’enregistrement recherché qui est lu. Le contrôle est immédiatement rendu, indiquant que la fin du <strong>Recordset</strong> a été atteinte. Par exemple, l’appel de <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> déplace l’enregistrement actuel et le définit comme dernier enregistrement réellement extrait, même si d’autres enregistrements continuent d’être ajoutés au <strong>Recordset</strong>.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>[!REMARQUE] Chaque fichier exécutable côté client utilisant ces constantes doit fournir les déclarations correspondantes. Vous pouvez couper et coller les déclarations de constante dont vous avez besoin dans le fichier Adcvbs.inc placé dans le dossier C:\Program Files\Common Files\System\MSADC.</P>



## <a name="remarks"></a>Remarques

<<<<<<< Tête dans une application Web, il est recommandé d’utiliser **adcFetchAsync** (la valeur par défaut), car elle offre de meilleures performances. Dans une application cliente compilée, on utilise généralement **adcFetchBackground**.
=== Dans une application web, il est recommandé d’utiliser **adcFetchAsync** (la valeur par défaut), car elle offre de meilleures performances. Dans une application cliente compilée, on utilise généralement **adcFetchBackground**.
>>>>>>> master

