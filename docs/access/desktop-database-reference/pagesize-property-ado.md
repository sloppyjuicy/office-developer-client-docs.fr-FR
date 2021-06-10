---
title: PageSize, propriété (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9365acb13820f898c053d4c90fc252bfd3b228c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288132"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="e2b81-102">PageSize, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="e2b81-102">PageSize property (ADO)</span></span>


<span data-ttu-id="e2b81-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2b81-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e2b81-104">Indique combien d’enregistrements constituent une page dans le [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e2b81-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e2b81-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e2b81-105">Settings and return values</span></span>

<span data-ttu-id="e2b81-p101">Définit ou retourne une valeur de type **Long** qui indique le nombre d'enregistrements sur une page. La valeur par défaut est 10.</span><span class="sxs-lookup"><span data-stu-id="e2b81-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2b81-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="e2b81-108">Remarks</span></span>

<span data-ttu-id="e2b81-109">La propriété **PageSize** permet de déterminer le nombre d'enregistrements constituant une page logique de données.</span><span class="sxs-lookup"><span data-stu-id="e2b81-109">Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="e2b81-110">La définition d'une taille de page vous permet d'utiliser la propriété [AbsolutePage](absolutepage-property-ado.md) pour accéder au premier enregistrement d'une page donnée.</span><span class="sxs-lookup"><span data-stu-id="e2b81-110">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="e2b81-111">Cela est utile dans les scénarios de serveur web lorsque vous souhaitez autoriser l’utilisateur à paginer des données, en visualant un certain nombre d’enregistrements à la fois.</span><span class="sxs-lookup"><span data-stu-id="e2b81-111">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="e2b81-112">Cette propriété peut être définie à tout moment et sa valeur sera utilisée pour calculer l'emplacement du premier enregistrement d'une page donnée.</span><span class="sxs-lookup"><span data-stu-id="e2b81-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

