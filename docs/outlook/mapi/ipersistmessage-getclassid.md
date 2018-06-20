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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e0937eed2e8ca61bc18ee45ff20337267808ea70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784355"
---
# <a name="ipersistmessagegetclassid"></a><span data-ttu-id="a62c6-103">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="a62c6-103">IPersistMessage::GetClassID</span></span>

  
  
<span data-ttu-id="a62c6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a62c6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a62c6-105">Renvoie un identificateur qui représente le serveur de formulaire qui peut gérer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="a62c6-105">Returns an identifier that represents the form server that can manage the form.</span></span> 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a><span data-ttu-id="a62c6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a62c6-106">Parameters</span></span>

 <span data-ttu-id="a62c6-107">_lpClassID_</span><span class="sxs-lookup"><span data-stu-id="a62c6-107">_lpClassID_</span></span>
  
> <span data-ttu-id="a62c6-108">[entrée, sortie] Pointeur vers l’identificateur de classe (CLSID) du formulaire.</span><span class="sxs-lookup"><span data-stu-id="a62c6-108">[in, out] A pointer to the class identifier (CLSID) of the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a62c6-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a62c6-109">Return value</span></span>

<span data-ttu-id="a62c6-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a62c6-110">S_OK</span></span> 
  
> <span data-ttu-id="a62c6-111">L’identificateur de classe a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="a62c6-111">The class identifier was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a62c6-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="a62c6-112">Remarks</span></span>

<span data-ttu-id="a62c6-113">La méthode **IPersistMessge::GetClassID** définit le contenu du paramètre _lpClassID_ sur l’identificateur de classe du serveur du formulaire et renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="a62c6-113">The **IPersistMessge::GetClassID** method sets the contents of the  _lpClassID_ parameter to the form server's class identifier and returns S_OK.</span></span> <span data-ttu-id="a62c6-114">Lorsqu’une visionneuse de formulaire appelle **GetClassID** et elle renvoie avec succès, le formulaire est placé dans l’état [Uninitialized](uninitialized-state.md) .</span><span class="sxs-lookup"><span data-stu-id="a62c6-114">When a form viewer calls **GetClassID** and it returns successfully, the form is placed in the [Uninitialized](uninitialized-state.md) state.</span></span> 
  
<span data-ttu-id="a62c6-115">Pour plus d’informations sur l’utilisation des identificateurs de classe des objets de stockage structuré, consultez la documentation de la méthode [IPersist::GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a62c6-115">For more information about how class identifiers are used with structured storage objects, see the documentation for the [IPersist::GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a62c6-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a62c6-116">See also</span></span>



[<span data-ttu-id="a62c6-117">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a62c6-117">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

