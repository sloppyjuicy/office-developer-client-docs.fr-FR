---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Représente l’identificateur d’entrée du dossier par défaut pour les éléments envoyés pour le compte.
ms.openlocfilehash: 7795e8a112f0575b764fd55e92d27c7085e3d3a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782805"
---
# <a name="propacctsentitemseid"></a><span data-ttu-id="5619e-103">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="5619e-103">PROP_ACCT_SENTITEMS_EID</span></span>

<span data-ttu-id="5619e-104">Représente l’identificateur d’entrée du dossier par défaut pour les éléments envoyés pour le compte.</span><span class="sxs-lookup"><span data-stu-id="5619e-104">Represents the Entry ID of the default folder for sent items for the account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="5619e-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="5619e-105">Quick info</span></span>

<span data-ttu-id="5619e-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="5619e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5619e-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5619e-107">Identifier:</span></span>  <br/> |<span data-ttu-id="5619e-108">0 x 0020</span><span class="sxs-lookup"><span data-stu-id="5619e-108">0x0020</span></span>  <br/> |
|<span data-ttu-id="5619e-109">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="5619e-109">Property type:</span></span>  <br/> |<span data-ttu-id="5619e-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5619e-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5619e-111">Balise de propriété :</span><span class="sxs-lookup"><span data-stu-id="5619e-111">Property tag:</span></span>  <br/> |<span data-ttu-id="5619e-112">0x00200102</span><span class="sxs-lookup"><span data-stu-id="5619e-112">0x00200102</span></span>  <br/> |
|<span data-ttu-id="5619e-113">Access :</span><span class="sxs-lookup"><span data-stu-id="5619e-113">Access:</span></span>  <br/> |<span data-ttu-id="5619e-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5619e-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5619e-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="5619e-115">Remarks</span></span>

<span data-ttu-id="5619e-116">Obtenez cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="5619e-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="5619e-117">Le dossier éléments envoyés par défaut est **Éléments envoyés**.</span><span class="sxs-lookup"><span data-stu-id="5619e-117">The default folder for sent items is **Sent Items**.</span></span>
  
<span data-ttu-id="5619e-118">Cette propriété est en lecture seule pour les comptes POP3 et IMAP.</span><span class="sxs-lookup"><span data-stu-id="5619e-118">This property is read-only for POP3 and IMAP accounts.</span></span> <span data-ttu-id="5619e-119">Essayez de définir cette propriété pour ces types de comptes renvoie **E_ACCT_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="5619e-119">Attempting to set this property for these types of accounts returns **E_ACCT_NOT_FOUND**.</span></span> 
  

