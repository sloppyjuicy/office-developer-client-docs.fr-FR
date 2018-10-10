---
title: ParentRow, propriété (ADO)
TOCTitle: ParentRow Property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 834dcaed7d1acdcf66410584436e2ccee8c91c56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472565"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="a93a6-102">ParentRow, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="a93a6-102">ParentRow Property (ADO)</span></span>


<span data-ttu-id="a93a6-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a93a6-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="a93a6-104">Indique que le conteneur d'un objet **Row** OLE DB est un objet **ADORecordConstruction**, ce qui indique que le parent de la ligne devient un objet **Record** ADO.</span><span class="sxs-lookup"><span data-stu-id="a93a6-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="a93a6-105">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="a93a6-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a93a6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a93a6-106">Syntax</span></span>

<span data-ttu-id="a93a6-107">Placer HRESULT\_ligne parente (\[dans\] IUnknown\* pParent) ;</span><span class="sxs-lookup"><span data-stu-id="a93a6-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="a93a6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a93a6-108">Parameters</span></span>

  - <span data-ttu-id="a93a6-109">*pParent*</span><span class="sxs-lookup"><span data-stu-id="a93a6-109">*pParent*</span></span>

  - <span data-ttu-id="a93a6-110">Le conteneur d'une ligne.</span><span class="sxs-lookup"><span data-stu-id="a93a6-110">A container of a row.</span></span>

## <a name="return-values"></a><span data-ttu-id="a93a6-111">Valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="a93a6-111">Return Values</span></span>

<span data-ttu-id="a93a6-112">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="a93a6-112">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a93a6-113">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="a93a6-113">Applies To</span></span>

[<span data-ttu-id="a93a6-114">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="a93a6-114">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

