---
title: À l’aide de Pages (référence de base de données du bureau Access)
TOCTitle: Using Pages
ms:assetid: 516fb7c2-c7a2-385b-83e7-2091c7283ea2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249261(v=office.15)
ms:contentKeyID: 48544817
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 795488f5e87c203a92eb2ba7ddddfef01a9d1f8d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947713"
---
# <a name="using-pages"></a><span data-ttu-id="65069-102">L’utilisation des pages</span><span class="sxs-lookup"><span data-stu-id="65069-102">Using pages</span></span>


<span data-ttu-id="65069-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65069-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="65069-104">Utilisez la propriété **PageCount** pour déterminer le nombre de pages que contient l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="65069-104">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="65069-105">*Les pages* sont des groupes d’enregistrements dont la taille est égale à **la propriété PageSize** .</span><span class="sxs-lookup"><span data-stu-id="65069-105">*Pages* are groups of records whose size equals the **PageSize** property setting.</span></span> <span data-ttu-id="65069-106">Même si la dernière page est incomplète et que le nombre d'enregistrements qu'elle contient est inférieur à la valeur de **PageSize**, elle est considérée comme une page supplémentaire dans la valeur **PageCount**.</span><span class="sxs-lookup"><span data-stu-id="65069-106">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="65069-107">Si l’objet **Recordset** ne prend pas en charge cette propriété, **PageCount** sera -1 pour indiquer que le **PageCount** est déterminé.</span><span class="sxs-lookup"><span data-stu-id="65069-107">If the **Recordset** object does not support this property, **PageCount** will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="65069-p102">La propriété **PageSize** permet de déterminer le nombre d'enregistrements constituant une page logique de données. La définition d'une taille de page vous permet d'utiliser la propriété **AbsolutePage** pour accéder au premier enregistrement d'une page donnée. Ceci s'avère utile dans les scénarios de serveurs Web, pour offrir aux utilisateurs la possibilité de passer d'une page de données à une autre et de consulter un certain nombre d'enregistrements à la fois.</span><span class="sxs-lookup"><span data-stu-id="65069-p102">Use the **PageSize** property to determine how many records make up a logical page of data. Establishing a page size allows you to use the **AbsolutePage** property to move to the first record of a particular page. This is useful in Web-server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="65069-111">Cette propriété peut être définie à tout moment et sa valeur sera utilisée pour calculer l'emplacement du premier enregistrement d'une page donnée.</span><span class="sxs-lookup"><span data-stu-id="65069-111">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

<span data-ttu-id="65069-p103">Utilisez la propriété **AbsolutePage** pour identifier le numéro de la page de l'enregistrement actif. Ici encore, le fournisseur doit prendre en charge les fonctionnalités requises pour que cette propriété soit disponible.</span><span class="sxs-lookup"><span data-stu-id="65069-p103">Use the **AbsolutePage** property to identify the page number on which the current record is located. Again, the provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="65069-p104">**AbsolutePage** utilise des nombres en base 1 et est égale à 1 lorsque l'enregistrement actif est le premier de l'objet **Recordset**. Définissez cette propriété pour accéder au premier enregistrement d'une page donnée. Le nombre total de pages est obtenu à l'aide de la propriété **PageCount**.</span><span class="sxs-lookup"><span data-stu-id="65069-p104">**AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**. Set this property to move to the first record of a particular page. Obtain the total number of pages from the **PageCount** property.</span></span>

