---
title: ParentRow, propriété (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2844f7c93164c4b384a895cd32a13bd682154ce3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287737"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="1309d-102">ParentRow, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="1309d-102">ParentRow property (ADO)</span></span>

<span data-ttu-id="1309d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1309d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1309d-104">Indique que le conteneur d'un objet **Row** OLE DB est un objet **ADORecordConstruction**, ce qui indique que le parent de la ligne devient un objet **Record** ADO.</span><span class="sxs-lookup"><span data-stu-id="1309d-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="1309d-105">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="1309d-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1309d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1309d-106">Syntax</span></span>

<span data-ttu-id="1309d-107">HRESULT put \_ ParentRow( \[ in \] IUnknown \* pParent);</span><span class="sxs-lookup"><span data-stu-id="1309d-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="1309d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1309d-108">Parameters</span></span>

|<span data-ttu-id="1309d-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1309d-109">Parameter</span></span>|<span data-ttu-id="1309d-110">Description</span><span class="sxs-lookup"><span data-stu-id="1309d-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1309d-111">*pParent*</span><span class="sxs-lookup"><span data-stu-id="1309d-111">*pParent*</span></span> |<span data-ttu-id="1309d-112">Le conteneur d'une ligne.</span><span class="sxs-lookup"><span data-stu-id="1309d-112">A container of a row.</span></span>|

## <a name="return-values"></a><span data-ttu-id="1309d-113">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="1309d-113">Return values</span></span>

<span data-ttu-id="1309d-114">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S \_ OK et E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="1309d-114">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1309d-115">S’applique à</span><span class="sxs-lookup"><span data-stu-id="1309d-115">Applies to</span></span>

[<span data-ttu-id="1309d-116">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="1309d-116">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

