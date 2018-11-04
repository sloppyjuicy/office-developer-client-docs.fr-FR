---
title: ParentRow, propriété (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06bb1110dfa7e7a055fa6cd863dcd2cc17f3f585
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950147"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="36b3c-102">ParentRow, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="36b3c-102">ParentRow property (ADO)</span></span>

<span data-ttu-id="36b3c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="36b3c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="36b3c-104">Indique que le conteneur d'un objet **Row** OLE DB est un objet **ADORecordConstruction**, ce qui indique que le parent de la ligne devient un objet **Record** ADO.</span><span class="sxs-lookup"><span data-stu-id="36b3c-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="36b3c-105">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="36b3c-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="36b3c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36b3c-106">Syntax</span></span>

<span data-ttu-id="36b3c-107">Placer HRESULT\_ligne parente (\[dans\] IUnknown\* pParent) ;</span><span class="sxs-lookup"><span data-stu-id="36b3c-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="36b3c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36b3c-108">Parameters</span></span>

|<span data-ttu-id="36b3c-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="36b3c-109">Parameter</span></span>|<span data-ttu-id="36b3c-110">Description</span><span class="sxs-lookup"><span data-stu-id="36b3c-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="36b3c-111">*pParent*</span><span class="sxs-lookup"><span data-stu-id="36b3c-111">*pParent*</span></span> |<span data-ttu-id="36b3c-112">Le conteneur d'une ligne.</span><span class="sxs-lookup"><span data-stu-id="36b3c-112">A container of a row.</span></span>|

## <a name="return-values"></a><span data-ttu-id="36b3c-113">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="36b3c-113">Return values</span></span>

<span data-ttu-id="36b3c-114">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="36b3c-114">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="36b3c-115">S’applique à</span><span class="sxs-lookup"><span data-stu-id="36b3c-115">Applies to</span></span>

[<span data-ttu-id="36b3c-116">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="36b3c-116">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

