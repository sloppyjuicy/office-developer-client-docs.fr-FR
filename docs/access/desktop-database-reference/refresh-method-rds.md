---
title: Refresh, méthode (RDS)
TOCTitle: Refresh method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 60de3b25e5eedc277eaafbe4bd1c078863e13f7b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718720"
---
# <a name="refresh-method-rds"></a><span data-ttu-id="f5c7e-102">Refresh, méthode (RDS)</span><span class="sxs-lookup"><span data-stu-id="f5c7e-102">Refresh method (RDS)</span></span>

<span data-ttu-id="f5c7e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5c7e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f5c7e-104">Interroge à nouveau la source de données spécifiée dans la propriété [Connect](connect-property-rds.md) et met à jour les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="f5c7e-104">Requeries the data source specified in the [Connect](connect-property-rds.md) property and updates the query results.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5c7e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5c7e-105">Syntax</span></span>

<span data-ttu-id="f5c7e-106">*DataControl*. Actualiser</span><span class="sxs-lookup"><span data-stu-id="f5c7e-106">*DataControl*.Refresh</span></span>

## <a name="parameters"></a><span data-ttu-id="f5c7e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="f5c7e-107">Parameters</span></span>

|<span data-ttu-id="f5c7e-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f5c7e-108">Parameter</span></span>|<span data-ttu-id="f5c7e-109">Description</span><span class="sxs-lookup"><span data-stu-id="f5c7e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f5c7e-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="f5c7e-110">*DataControl*</span></span> |<span data-ttu-id="f5c7e-111">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="f5c7e-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f5c7e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f5c7e-112">Remarks</span></span>

<span data-ttu-id="f5c7e-p101">Vous devez définir les propriétés [Connect](connect-property-rds.md), [Server](server-property-rds.md) et [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) avant d'utiliser la méthode **Refresh**. Tous les contrôles liés aux données présents sur le formulaire associé à un objet **RDS.DataControl** refléteront le nouveau jeu d'enregistrements. Tout objet [Recordset](recordset-object-ado.md) préexistant est libéré et les modifications non enregistrées sont ignorées. La méthode **Refresh** fait automatiquement du premier enregistrement l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="f5c7e-p101">You must set the [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) properties before you use the **Refresh** method. All data-bound controls on the form associated with an **RDS.DataControl** object will reflect the new set of records. Any pre-existing [Recordset](recordset-object-ado.md) object is released, and any unsaved changes are discarded. The **Refresh** method automatically makes the first record the current record.</span></span>

<span data-ttu-id="f5c7e-p102">Il est conseillé d'appeler régulièrement la méthode **Refresh** lorsque vous manipulez des données. Si vous récupérez des données et que vous les laissez pendant un certain temps sur votre ordinateur client, il est fort possible qu'elles ne soient plus à jour. Il se peut que certaines de vos modifications échouent si un autre utilisateur modifie l'enregistrement et valide les modifications avant vous.</span><span class="sxs-lookup"><span data-stu-id="f5c7e-p102">It's a good idea to call the **Refresh** method periodically when you work with data. If you retrieve data, and then leave it on your client machine for a while, it is likely to become out of date. It's possible that any changes you make will fail, because someone else might have changed the record and submitted changes before you.</span></span>

