---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3f0d98b8ffa13fe238fc0fcf8ff0ec76a3a284eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309624"
---
# <a name="ipersistmessagegetclassid"></a><span data-ttu-id="9a5fc-103">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="9a5fc-103">IPersistMessage::GetClassID</span></span>

  
  
<span data-ttu-id="9a5fc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a5fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a5fc-105">Renvoie un identificateur qui représente le serveur de formulaires qui peut gérer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="9a5fc-105">Returns an identifier that represents the form server that can manage the form.</span></span> 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a><span data-ttu-id="9a5fc-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9a5fc-106">Parameters</span></span>

 <span data-ttu-id="9a5fc-107">_lpClassID_</span><span class="sxs-lookup"><span data-stu-id="9a5fc-107">_lpClassID_</span></span>
  
> <span data-ttu-id="9a5fc-108">[in, out] Pointeur vers l’identificateur de classe (CLSID) du formulaire.</span><span class="sxs-lookup"><span data-stu-id="9a5fc-108">[in, out] A pointer to the class identifier (CLSID) of the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9a5fc-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9a5fc-109">Return value</span></span>

<span data-ttu-id="9a5fc-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="9a5fc-110">S_OK</span></span> 
  
> <span data-ttu-id="9a5fc-111">L’identificateur de classe a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="9a5fc-111">The class identifier was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a5fc-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="9a5fc-112">Remarks</span></span>

<span data-ttu-id="9a5fc-113">La **méthode IPersistMessge::GetClassID** définit le contenu du paramètre  _lpClassID_ sur l’identificateur de classe du serveur de formulaire et renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="9a5fc-113">The **IPersistMessge::GetClassID** method sets the contents of the  _lpClassID_ parameter to the form server's class identifier and returns S_OK.</span></span> <span data-ttu-id="9a5fc-114">Lorsqu’une visionneuse de formulaire appelle **GetClassID** et qu’elle renvoie correctement, le formulaire est placé dans [l’état Nonnitialisé.](uninitialized-state.md)</span><span class="sxs-lookup"><span data-stu-id="9a5fc-114">When a form viewer calls **GetClassID** and it returns successfully, the form is placed in the [Uninitialized](uninitialized-state.md) state.</span></span> 
  
<span data-ttu-id="9a5fc-115">Pour plus d’informations sur l’utilisation des identificateurs de classe avec des objets de stockage structuré, voir la documentation de la méthode [IPersist::GetClassID.](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a5fc-115">For more information about how class identifiers are used with structured storage objects, see the documentation for the [IPersist::GetClassID](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a5fc-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a5fc-116">See also</span></span>



[<span data-ttu-id="9a5fc-117">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a5fc-117">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

