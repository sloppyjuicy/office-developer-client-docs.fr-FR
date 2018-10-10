---
title: PageSize, propriété (ADO)
TOCTitle: PageSize Property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89b28e382f1597ff6466aa323565eaf2ff068605
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469484"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="b7c82-102">PageSize, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="b7c82-102">PageSize Property (ADO)</span></span>


<span data-ttu-id="b7c82-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7c82-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b7c82-104">Indique combien d'enregistrements constituent une page dans le [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b7c82-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b7c82-105">Paramètres et valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="b7c82-105">Settings and Return Values</span></span>

<span data-ttu-id="b7c82-p101">Définit ou retourne une valeur de type **Long** qui indique le nombre d'enregistrements sur une page. La valeur par défaut est 10.</span><span class="sxs-lookup"><span data-stu-id="b7c82-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7c82-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="b7c82-108">Remarks</span></span>

<span data-ttu-id="b7c82-p102">La propriété **PageSize** permet de déterminer le nombre d'enregistrements constituant une page logique de données. La définition d'une taille de page vous permet d'utiliser la propriété [AbsolutePage](absolutepage-property-ado.md) pour accéder au premier enregistrement d'une page donnée. Ceci s'avère utile dans les scénarios de serveurs Web, pour offrir aux utilisateurs la possibilité de passer d'une page de données à une autre et de consulter un certain nombre d'enregistrements à la fois.</span><span class="sxs-lookup"><span data-stu-id="b7c82-p102">Use the **PageSize** property to determine how many records make up a logical page of data. Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page. This is useful in Web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="b7c82-112">Cette propriété peut être définie à tout moment ; sa valeur est utilisée pour calculer l'emplacement du premier enregistrement d'une page donnée.</span><span class="sxs-lookup"><span data-stu-id="b7c82-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

