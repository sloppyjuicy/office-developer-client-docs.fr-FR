---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: 'Dernière modification: 24 février 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279534"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="e862a-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="e862a-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="e862a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e862a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e862a-105">Lance la procédure de déverrouillage pour un fichier de dossiers personnels (. pst).</span><span class="sxs-lookup"><span data-stu-id="e862a-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="e862a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e862a-106">Parameters</span></span>

 <span data-ttu-id="e862a-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="e862a-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="e862a-108">dans Pointeur vers le chemin d'accès d'une bibliothèque de liens dynamiques (DLL) tierce.</span><span class="sxs-lookup"><span data-stu-id="e862a-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="e862a-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="e862a-109">_pvClientData_</span></span>
  
> <span data-ttu-id="e862a-110">dans Pointeur vers les données client, qui sera transmis par le fournisseur PST dans les appels ultérieurs à la fonction HrTrustedPSTOverrideHandlerCallback de la DLL.</span><span class="sxs-lookup"><span data-stu-id="e862a-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="e862a-111">Ces données client peuvent être utilisées par la DLL pour vérifier si le fichier PST doit être déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="e862a-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e862a-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e862a-112">Return value</span></span>

<span data-ttu-id="e862a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e862a-113">S_OK</span></span>
  
> <span data-ttu-id="e862a-114">L'appel de la fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="e862a-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e862a-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="e862a-115">Remarks</span></span>

<span data-ttu-id="e862a-116">La DLL spécifiée par le paramètre wzDllPath doit être signée à l'aide d'un certificat numérique.</span><span class="sxs-lookup"><span data-stu-id="e862a-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="e862a-117">La DLL doit également exporter une fonction avec la signature suivante.</span><span class="sxs-lookup"><span data-stu-id="e862a-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="e862a-118">Cette fonction est appelée avec un pointeur vers l'objet IMsgStore pour le fichier PST, un pointeur vers un objet IUnknown qui implémente l'interface IPSTOVERRIDE1 et un pointeur vers les données initialement fournies par le biais de pvClientData.</span><span class="sxs-lookup"><span data-stu-id="e862a-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="e862a-119">Pour plus d'informations, reportez-vous à la rubrique [implémentation d'un gestionnaire de substitution PST pour contourner la stratégie PSTDisableGrow dans Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="e862a-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e862a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e862a-120">See also</span></span>



[<span data-ttu-id="e862a-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e862a-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="e862a-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e862a-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

