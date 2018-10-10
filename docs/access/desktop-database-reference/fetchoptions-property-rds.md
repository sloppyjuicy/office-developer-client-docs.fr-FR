---
title: FetchOptions, propriété (RDS)
TOCTitle: FetchOptions Property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 60eb05d87e7d31d283cdcf29c0f6240892fe29ef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470500"
---
# <a name="fetchoptions-property-rds"></a><span data-ttu-id="f8c81-102">FetchOptions, propriété (RDS)</span><span class="sxs-lookup"><span data-stu-id="f8c81-102">FetchOptions Property (RDS)</span></span>


<span data-ttu-id="f8c81-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8c81-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f8c81-104">Indique le type d'extraction asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f8c81-104">Indicates the type of asynchronous fetching.</span></span>

## <a name="setting-and-return-values"></a><span data-ttu-id="f8c81-105">Paramètre et valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f8c81-105">Setting and Return Values</span></span>

<span data-ttu-id="f8c81-106">Définit ou renvoie l'une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f8c81-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f8c81-107">Constante</span><span class="sxs-lookup"><span data-stu-id="f8c81-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="f8c81-108">Description</span><span class="sxs-lookup"><span data-stu-id="f8c81-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8c81-109"><strong>valeur adcFetchUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="f8c81-109"><strong>adcFetchUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="f8c81-p101">Tous les enregistrements du <a href="recordset-object-ado.md">Recordset</a> sont extraits avant que le contrôle ne soit renvoyé à l’application. L’objet <strong>Recordset</strong> complet est extrait avant que l’application ne puisse en faire quoi que ce soit.</span><span class="sxs-lookup"><span data-stu-id="f8c81-p101">All the records of the <a href="recordset-object-ado.md">Recordset</a> are fetched before control is returned to the application. The complete <strong>Recordset</strong> is fetched before the application is allowed to do anything with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8c81-112"><strong>adcFetchBackground</strong></span><span class="sxs-lookup"><span data-stu-id="f8c81-112"><strong>adcFetchBackground</strong></span></span></p></td>
<td><p><span data-ttu-id="f8c81-p102">Le contrôle est rendu à l'application dès que le premier lot d'enregistrements a été extrait. La demande suivante de lecture d'un <strong>Recordset</strong> non extrait dans le premier lot est retardée jusqu'à ce que l'enregistrement concerné soit extrait ; le contrôle revient alors à l'application.</span><span class="sxs-lookup"><span data-stu-id="f8c81-p102">Control can return to the application as soon as the first batch of records has been fetched. A subsequent read of the <strong>Recordset</strong> that attempts to access a record not fetched in the first batch will be delayed until the sought record is actually fetched, at which time control returns to the application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8c81-115"><strong>adcFetchAsync</strong></span><span class="sxs-lookup"><span data-stu-id="f8c81-115"><strong>adcFetchAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="f8c81-p103">Valeur par défaut. Le contrôle est immédiatement rendu à l’application pendant que des enregistrements sont extraits en arrière-plan. Si l’application tente de lire un enregistrement qui n’a pas encore été extrait, c’est l’enregistrement le plus proche de l’enregistrement recherché qui est lu. Le contrôle est immédiatement rendu, indiquant que la fin du <strong>Recordset</strong> a été atteinte. Par exemple, l’appel de <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> déplace l’enregistrement actuel et le définit comme dernier enregistrement réellement extrait, même si d’autres enregistrements continuent d’être ajoutés au <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="f8c81-p103">Default. Control returns immediately to the application while records are fetched in the background. If the application attempts to read a record that hasn't yet been fetched, the record closest to the sought record will be read and control will return immediately, indicating that the current end of the <strong>Recordset</strong> has been reached. For example, a call to <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> will move the current record position to the last record actually fetched, even though more records will continue to populate the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="f8c81-p104">[!REMARQUE] Chaque fichier exécutable côté client utilisant ces constantes doit fournir les déclarations correspondantes. Vous pouvez couper et coller les déclarations de constante dont vous avez besoin dans le fichier Adcvbs.inc placé dans le dossier C:\Program Files\Common Files\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="f8c81-p104">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="f8c81-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="f8c81-122">Remarks</span></span>

<span data-ttu-id="f8c81-p105">Dans une application Web, on utilise généralement **adcFetchAsync** (la valeur par défaut), parce qu'elle offre de meilleures performances. Dans une application cliente compilée, on utilise généralement **adcFetchBackground**.</span><span class="sxs-lookup"><span data-stu-id="f8c81-p105">In a Web application, you will usually want to use **adcFetchAsync** (the default value), because it provides better performance. In a compiled client application, you will usually want to use **adcFetchBackground**.</span></span>

