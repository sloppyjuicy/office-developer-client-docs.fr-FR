---
title: HrGetAutoDiscoverXML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 77f28654ffe0f6f459fde229bb7428f2c39e96c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347802"
---
# <a name="hrgetautodiscoverxml"></a><span data-ttu-id="bc745-103">HrGetAutoDiscoverXML</span><span class="sxs-lookup"><span data-stu-id="bc745-103">HrGetAutoDiscoverXML</span></span>

  
  
<span data-ttu-id="bc745-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc745-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc745-105">Renvoie un flux XML (Extensible Markup Language) qui représente des informations extraites du service de découverte automatique d'un serveur Microsoft Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="bc745-105">Returns an Extensible Markup Language (XML) stream that represents information retrieved from the auto-discovery service of a Microsoft Exchange 2007 server.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bc745-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="bc745-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc745-107">Exporté par:</span><span class="sxs-lookup"><span data-stu-id="bc745-107">Exported by:</span></span>  <br/> |<span data-ttu-id="bc745-108">olmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="bc745-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="bc745-109">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="bc745-109">Called by:</span></span>  <br/> |<span data-ttu-id="bc745-110">Client</span><span class="sxs-lookup"><span data-stu-id="bc745-110">Client</span></span>  <br/> |
|<span data-ttu-id="bc745-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="bc745-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="bc745-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="bc745-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a><span data-ttu-id="bc745-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc745-113">Parameters</span></span>

 <span data-ttu-id="bc745-114">_pwzAddress_</span><span class="sxs-lookup"><span data-stu-id="bc745-114">_pwzAddress_</span></span>
  
> <span data-ttu-id="bc745-115">dans Adresse de messagerie SMTP (Simple Mail Transfer Protocol) du compte pour lequel vous souhaitez récupérer les informations de découverte automatique.</span><span class="sxs-lookup"><span data-stu-id="bc745-115">[in] A null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.</span></span>
    
 <span data-ttu-id="bc745-116">_pwzPassword_</span><span class="sxs-lookup"><span data-stu-id="bc745-116">_pwzPassword_</span></span>
  
> <span data-ttu-id="bc745-117">dans Mot de passe facultatif pour le compte spécifié par _pwzAddress_.</span><span class="sxs-lookup"><span data-stu-id="bc745-117">[in] An optional password for the account specified by  _pwzAddress_.</span></span> <span data-ttu-id="bc745-118">Notez que le passage de n'importe quel mot de passe n'a aucun effet si le compte spécifié par _pwzAddress_ ne requiert pas de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="bc745-118">Note that passing any password has no effect if the account specified by  _pwzAddress_ does not require a password.</span></span> 
    
 <span data-ttu-id="bc745-119">_hCancelEvent_</span><span class="sxs-lookup"><span data-stu-id="bc745-119">_hCancelEvent_</span></span>
  
> <span data-ttu-id="bc745-120">dans Un descripteur d'événement Win32 non défini qui est facultatif et qui peut être utilisé pour annuler l'opération.</span><span class="sxs-lookup"><span data-stu-id="bc745-120">[in] An unset Win32 event handle that is optional and can be used to cancel the operation.</span></span> <span data-ttu-id="bc745-121">Pour annuler l'opération, définissez l'événement et transmettez le descripteur d'événement en tant que _hCancelEvent_; transmettez la **valeur null** si vous ne souhaitez pas annuler l'opération.</span><span class="sxs-lookup"><span data-stu-id="bc745-121">To cancel the operation, set the event and pass the event handle as  _hCancelEvent_; pass **null** if you do not want to cancel the operation.</span></span> <span data-ttu-id="bc745-122">Notez que le passage d'une valeur qui ne représente pas un descripteur d'événement n'a aucun effet et est ignoré par la fonction.</span><span class="sxs-lookup"><span data-stu-id="bc745-122">Note that passing a value that does not represent an event handle has no effect and is ignored by the function.</span></span> 
    
 <span data-ttu-id="bc745-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bc745-123">_ulFlags_</span></span>
  
> <span data-ttu-id="bc745-124">dans Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="bc745-124">[in] This parameter is not used.</span></span> <span data-ttu-id="bc745-125">Il doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="bc745-125">It must be 0.</span></span>
    
 <span data-ttu-id="bc745-126">_ppXmlStream_</span><span class="sxs-lookup"><span data-stu-id="bc745-126">_ppXmlStream_</span></span>
  
> <span data-ttu-id="bc745-127">remarquer Pointeur vers un objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) qui contient le code XML de découverte automatique.</span><span class="sxs-lookup"><span data-stu-id="bc745-127">[out] A pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object that contains the autodiscovery XML.</span></span> <span data-ttu-id="bc745-128">Renvoie la **valeur null** si l'opération de découverte automatique échoue.</span><span class="sxs-lookup"><span data-stu-id="bc745-128">Returns **null** if the autodiscovery operation fails.</span></span> <span data-ttu-id="bc745-129">Vous devez libérer l'objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) une fois que vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="bc745-129">You must release the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object when you are finished with it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="bc745-130">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="bc745-130">Return values</span></span>

<span data-ttu-id="bc745-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc745-131">S_OK</span></span> 
  
- <span data-ttu-id="bc745-132">L'appel de fonction est réussi.</span><span class="sxs-lookup"><span data-stu-id="bc745-132">The function call is successful.</span></span>
    
<span data-ttu-id="bc745-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="bc745-133">E_INVALIDARG</span></span> 
  
-  <span data-ttu-id="bc745-134">_pwzAddress_ est **null** ou n'est pas une adresse SMTP valide, ou _ppXmlStream_ est un pointeur **null** vers un objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="bc745-134">_pwzAddress_ is **null** or is not a valid SMTP address, or  _ppXmlStream_ is a **null** pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object.</span></span> 
    
<span data-ttu-id="bc745-135">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="bc745-135">MAPI_E_NOT_FOUND</span></span> 
  
- <span data-ttu-id="bc745-136">L'ordinateur client n'est pas connecté au réseau, l'ordinateur client n'est pas connecté à un serveur Microsoft Exchange 2007, _pwzAddress_ n'est pas un compte sur un serveur Exchange 2007 ou _pwzAddress_ est un compte qui ne prend pas en charge Exchange service de découverte automatique.</span><span class="sxs-lookup"><span data-stu-id="bc745-136">Client computer is not connected to the network, client computer is not connected to a Microsoft Exchange 2007 server,  _pwzAddress_ is not an account on an Exchange 2007 server, or  _pwzAddress_ is an account that does not support Exchange auto-discovery service.</span></span> 
    
<span data-ttu-id="bc745-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="bc745-137">MAPI_E_USER_CANCEL</span></span> 
  
- <span data-ttu-id="bc745-138">Un descripteur d'événement a été transmis à _hCancelEvent_ pour annuler l'opération.</span><span class="sxs-lookup"><span data-stu-id="bc745-138">An event handle has been passed to  _hCancelEvent_ to cancel the operation.</span></span> 
    
<span data-ttu-id="bc745-139">STRSAFE_E_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="bc745-139">STRSAFE_E_INSUFFICIENT_BUFFER</span></span>
  
- <span data-ttu-id="bc745-140">La valeur transmise à _pwzAddress_ ou _pwzPassword_ est trop longue, de sorte qu'elle déborde de la mémoire tampon interne de taille 256 octets.</span><span class="sxs-lookup"><span data-stu-id="bc745-140">The value passed to  _pwzAddress_ or  _pwzPassword_ is too long, such that it overflows the internal buffer of size 256 bytes.</span></span> 
    

