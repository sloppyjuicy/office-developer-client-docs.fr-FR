---
title: ParentRow, propriété (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28f0d1c7dbc0e062ff133b9f9997f1a737c3262e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872129"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="9ea58-102">ParentRow, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="9ea58-102">ParentRow property (ADO)</span></span>


<span data-ttu-id="9ea58-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ea58-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="9ea58-104">Indique que le conteneur d'un objet **Row** OLE DB est un objet **ADORecordConstruction**, ce qui indique que le parent de la ligne devient un objet **Record** ADO.</span><span class="sxs-lookup"><span data-stu-id="9ea58-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="9ea58-105">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="9ea58-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ea58-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ea58-106">Syntax</span></span>

<span data-ttu-id="9ea58-107">Placer HRESULT\_ligne parente (\[dans\] IUnknown\* pParent) ;</span><span class="sxs-lookup"><span data-stu-id="9ea58-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="9ea58-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ea58-108">Parameters</span></span>

  - <span data-ttu-id="9ea58-109">*pParent*</span><span class="sxs-lookup"><span data-stu-id="9ea58-109">*pParent*</span></span>

  - <span data-ttu-id="9ea58-110">Le conteneur d'une ligne.</span><span class="sxs-lookup"><span data-stu-id="9ea58-110">A container of a row.</span></span>

## <a name="return-values"></a><span data-ttu-id="9ea58-111">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="9ea58-111">Return values</span></span>

<span data-ttu-id="9ea58-112">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="9ea58-112">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9ea58-113">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="9ea58-113">Applies To</span></span>

[<span data-ttu-id="9ea58-114">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="9ea58-114">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

