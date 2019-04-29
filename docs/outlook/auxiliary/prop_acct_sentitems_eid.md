---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Représente l'ID d'entrée du dossier par défaut pour les éléments envoyés pour le compte.
ms.openlocfilehash: 24bb4714a4f4964ac3d84ea7a792e64da67599df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431840"
---
# <a name="propacctsentitemseid"></a><span data-ttu-id="39ab8-103">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="39ab8-103">PROP_ACCT_SENTITEMS_EID</span></span>

<span data-ttu-id="39ab8-104">Représente l'ID d'entrée du dossier par défaut pour les éléments envoyés pour le compte.</span><span class="sxs-lookup"><span data-stu-id="39ab8-104">Represents the Entry ID of the default folder for sent items for the account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="39ab8-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="39ab8-105">Quick info</span></span>

<span data-ttu-id="39ab8-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="39ab8-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="39ab8-107">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="39ab8-107">Identifier:</span></span>  <br/> |<span data-ttu-id="39ab8-108">0x0020</span><span class="sxs-lookup"><span data-stu-id="39ab8-108">0x0020</span></span>  <br/> |
|<span data-ttu-id="39ab8-109">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="39ab8-109">Property type:</span></span>  <br/> |<span data-ttu-id="39ab8-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="39ab8-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="39ab8-111">Balise de propriété:</span><span class="sxs-lookup"><span data-stu-id="39ab8-111">Property tag:</span></span>  <br/> |<span data-ttu-id="39ab8-112">0x00200102</span><span class="sxs-lookup"><span data-stu-id="39ab8-112">0x00200102</span></span>  <br/> |
|<span data-ttu-id="39ab8-113">Access</span><span class="sxs-lookup"><span data-stu-id="39ab8-113">Access:</span></span>  <br/> |<span data-ttu-id="39ab8-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="39ab8-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39ab8-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="39ab8-115">Remarks</span></span>

<span data-ttu-id="39ab8-116">Obtenez cette propriété à l'aide de [IOlkAccount:: getprop](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="39ab8-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="39ab8-117">Le dossier par défaut pour les éléments envoyés est **éléments envoyés**.</span><span class="sxs-lookup"><span data-stu-id="39ab8-117">The default folder for sent items is **Sent Items**.</span></span>
  
<span data-ttu-id="39ab8-118">Cette propriété est en lecture seule pour les comptes POP3 et IMAP.</span><span class="sxs-lookup"><span data-stu-id="39ab8-118">This property is read-only for POP3 and IMAP accounts.</span></span> <span data-ttu-id="39ab8-119">La tentative de définition de cette propriété pour ces types de comptes renvoie **E_ACCT_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="39ab8-119">Attempting to set this property for these types of accounts returns **E_ACCT_NOT_FOUND**.</span></span> 
  

