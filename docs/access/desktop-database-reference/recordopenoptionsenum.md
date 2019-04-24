---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caaf755ebd63f1805d0c77ef79a0f5863a85050e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300685"
---
# <a name="recordopenoptionsenum"></a><span data-ttu-id="8ac35-102">RecordOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="8ac35-102">RecordOpenOptionsEnum</span></span>


<span data-ttu-id="8ac35-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ac35-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ac35-104">Spécifie des options pour l'ouverture d'un [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8ac35-104">Specifies options for opening a [Record](record-object-ado.md).</span></span> <span data-ttu-id="8ac35-105">Les valeurs peuvent être combinées en utilisant OR.</span><span class="sxs-lookup"><span data-stu-id="8ac35-105">These values may be combined by using OR.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ac35-106">Constante</span><span class="sxs-lookup"><span data-stu-id="8ac35-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="8ac35-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ac35-107">Value</span></span></p></th>
<th><p><span data-ttu-id="8ac35-108">Description</span><span class="sxs-lookup"><span data-stu-id="8ac35-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ac35-109"><strong>adDelayFetchFields</strong></span><span class="sxs-lookup"><span data-stu-id="8ac35-109"><strong>adDelayFetchFields</strong></span></span></p></td>
<td><p><span data-ttu-id="8ac35-110">0x8000</span><span class="sxs-lookup"><span data-stu-id="8ac35-110">0x8000</span></span></p></td>
<td><p><span data-ttu-id="8ac35-p102">Indique au fournisseur que les champs associés au <strong>Record</strong> n'ont pas besoin d'être extraits tout de suite ; ils peuvent l'être à la première tentative d'accès. Le fonctionnement par défaut, indiqué par l'absence de cet indicateur, est d'extraire tous les champs de l'objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="8ac35-p102">Indicates to the provider that the fields associated with the <strong>Record</strong> need not be retrieved initially, but can be retrieved at the first attempt to access the field. The default behavior, indicated by the absence of this flag, is to retrieve all the <strong>Record</strong> object fields.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ac35-113"><strong>adDelayFetchStream</strong></span><span class="sxs-lookup"><span data-stu-id="8ac35-113"><strong>adDelayFetchStream</strong></span></span></p></td>
<td><p><span data-ttu-id="8ac35-114">0x4000</span><span class="sxs-lookup"><span data-stu-id="8ac35-114">0x4000</span></span></p></td>
<td><p><span data-ttu-id="8ac35-p103">Indique au fournisseur que la chaîne de données par défaut associée au <strong>Record</strong> n'a pas besoin d'être extraite tout de suite. Le fonctionnement par défaut, indiqué par l'absence de cet indicateur, est d'extraire la chaîne par défaut associée à l'objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="8ac35-p103">Indicates to the provider that the default stream associated with the <strong>Record</strong> need not be retrieved initially. The default behavior, indicated by the absence of this flag, is to retrieve the default stream associated with the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ac35-117"><strong>adOpenAsync</strong></span><span class="sxs-lookup"><span data-stu-id="8ac35-117"><strong>adOpenAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="8ac35-118">0x1000</span><span class="sxs-lookup"><span data-stu-id="8ac35-118">0x1000</span></span></p></td>
<td><p><span data-ttu-id="8ac35-119">Indique que l’objet <strong>Record</strong> est ouvert en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="8ac35-119">Indicates that the <strong>Record</strong> object is opened in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ac35-120"><strong>adOpenExecuteCommand</strong></span><span class="sxs-lookup"><span data-stu-id="8ac35-120"><strong>adOpenExecuteCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="8ac35-121">0x10000</span><span class="sxs-lookup"><span data-stu-id="8ac35-121">0x10000</span></span></p></td>
<td><p><span data-ttu-id="8ac35-p104">Indique que la chaîne source contient le texte des commandes qui doivent être exécutées. Cette valeur est équivalente à l'option <strong>adCmdText</strong> de <strong>Recordset.Open</strong>.</span><span class="sxs-lookup"><span data-stu-id="8ac35-p104">Indicates that the Source string contains command text that should be executed. This value is equivalent to the <strong>adCmdText</strong> option on <strong>Recordset.Open</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ac35-124"><strong>adOpenRecordUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="8ac35-124"><strong>adOpenRecordUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="8ac35-125">-1</span><span class="sxs-lookup"><span data-stu-id="8ac35-125">-1</span></span></p></td>
<td><p><span data-ttu-id="8ac35-p105">Par défaut. Indique qu'aucune option n'est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8ac35-p105">Default. Indicates no options are specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ac35-128"><strong>adOpenOutput</strong></span><span class="sxs-lookup"><span data-stu-id="8ac35-128"><strong>adOpenOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="8ac35-129">0x800000</span><span class="sxs-lookup"><span data-stu-id="8ac35-129">0x800000</span></span></p></td>
<td><p><span data-ttu-id="8ac35-p106">Indique que si la source pointe sur un nœud contenant un script exécutable (comme une page .ASP), le <strong>Record</strong> ouvert contiendra le résultat de ce script. Cette valeur n'est valide qu'avec les enregistrements sans collection.</span><span class="sxs-lookup"><span data-stu-id="8ac35-p106">Indicates that if the source points to a node that contains an executable script (such as an .ASP page), then the opened <strong>Record</strong> will contain the results of the executed script. This value is only valid with non-collection records.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8ac35-132">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8ac35-132">ADO/WFC equivalent</span></span>

<span data-ttu-id="8ac35-133">Ces constantes ne possèdent pas d'équivalent ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="8ac35-133">These constants do not have ADO/WFC equivalents.</span></span>

