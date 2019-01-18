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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709550"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="f3211-102">PageSize, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="f3211-102">PageSize property (ADO)</span></span>


<span data-ttu-id="f3211-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3211-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f3211-104">Indique combien d'enregistrements constituent une page dans le [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f3211-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f3211-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="f3211-105">Settings and return values</span></span>

<span data-ttu-id="f3211-p101">Définit ou retourne une valeur de type **Long** qui indique le nombre d'enregistrements sur une page. La valeur par défaut est 10.</span><span class="sxs-lookup"><span data-stu-id="f3211-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3211-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3211-108">Remarks</span></span>

<span data-ttu-id="f3211-109">La propriété **PageSize** permet de déterminer le nombre d'enregistrements constituant une page logique de données.</span><span class="sxs-lookup"><span data-stu-id="f3211-109">Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="f3211-110">La définition d'une taille de page vous permet d'utiliser la propriété [AbsolutePage](absolutepage-property-ado.md) pour accéder au premier enregistrement d'une page donnée.</span><span class="sxs-lookup"><span data-stu-id="f3211-110">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="f3211-111">Cela est utile dans les scénarios de serveur web lorsque vous souhaitez permettre à l’utilisateur de parcourir les données, consulter un certain nombre d’enregistrements à la fois.</span><span class="sxs-lookup"><span data-stu-id="f3211-111">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="f3211-112">Cette propriété peut être définie à tout moment ; sa valeur est utilisée pour calculer l'emplacement du premier enregistrement d'une page donnée.</span><span class="sxs-lookup"><span data-stu-id="f3211-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

