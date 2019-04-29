---
title: Éléments d'API déConseillés dans cette édition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: abfe734ad8af436f52fc0308d0cd236078bb47df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436887"
---
# <a name="api-elements-deprecated-in-this-edition"></a><span data-ttu-id="4028e-103">Éléments d'API déConseillés dans cette édition</span><span class="sxs-lookup"><span data-stu-id="4028e-103">API Elements Deprecated in This Edition</span></span>

  
  
<span data-ttu-id="4028e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4028e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4028e-105">Les éléments d'API suivants sont déconseillés dans Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="4028e-105">The following API elements are deprecated in Microsoft Outlook 2013.</span></span> <span data-ttu-id="4028e-106">Elles ne sont plus prises en charge et vous ne devez pas les utiliser dans de nouveaux projets.</span><span class="sxs-lookup"><span data-stu-id="4028e-106">They are no longer supported and you should not use them in new projects.</span></span>
  
## <a name="deprecation-of-message-and-recipient-options"></a><span data-ttu-id="4028e-107">DésApprobation des options de message et de destinataire</span><span class="sxs-lookup"><span data-stu-id="4028e-107">Deprecation of Message and Recipient Options</span></span>

<span data-ttu-id="4028e-108">Les éléments d'API suivants sont déconseillés dans cette version en raison des options de message et de destinataire obsolètes:</span><span class="sxs-lookup"><span data-stu-id="4028e-108">The following API elements are deprecated in this release because of obsolete message and recipient options:</span></span>
  
- <span data-ttu-id="4028e-109">**IXPLogon:: RegisterOptions**— le sous-système MAPI n'appelle plus cette méthode pour établir des valeurs par défaut pour les options de message et de destinataire d'un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="4028e-109">**IXPLogon::RegisterOptions**—The MAPI subsystem no longer calls this method to establish any default values for message and recipient options for a transport provider.</span></span>
    
- <span data-ttu-id="4028e-110">\*\*\*\* La structure de données qui prend en charge les propriétés des options de message et de destinataire est obsolète.</span><span class="sxs-lookup"><span data-stu-id="4028e-110">**OPTIONDATA**—This data structure that supported properties for message and recipient options is obsolete.</span></span> <span data-ttu-id="4028e-111">Le sous-système MAPI n'appelle plus **IXPLogon:: RegisterOptions** pour obtenir les options de message ou de destinataire prises en charge par un fournisseur de transport pour un type d'adresse particulier.</span><span class="sxs-lookup"><span data-stu-id="4028e-111">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** to obtain any message or recipient options that a transport provider supports for a particular address type.</span></span> 
    
- <span data-ttu-id="4028e-112">**OPTIONCALLBACK**: ce prototype de fonction, qu'un fournisseur de transport a utilisé pour déclarer une fonction de rappel et qui, à son tour, le sous-système MAPI utilisé pour résoudre les propriétés du fournisseur, est obsolète.</span><span class="sxs-lookup"><span data-stu-id="4028e-112">**OPTIONCALLBACK**—This function prototype, which a transport provider used to declare a callback function and which, in turn, the MAPI subsystem used to resolve the provider's properties, is obsolete.</span></span> <span data-ttu-id="4028e-113">Le sous-système MAPI n'appelle plus **IXPLogon:: RegisterOptions** ou utilise une fonction de rappel renvoyée par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="4028e-113">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** or uses any callback function returned by the transport provider.</span></span> 
    
- <span data-ttu-id="4028e-114">**IMAPISession:: MessageOptions**: les fournisseurs de services et clients MAPI ne doivent plus appeler cette méthode pour afficher les propriétés ou permettre aux utilisateurs de définir des propriétés qui contrôlent un message et un type d'adresse spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4028e-114">**IMAPISession::MessageOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control a particular message and address type.</span></span> <span data-ttu-id="4028e-115">La méthode renvoie toujours MAPI_E_NOT_FOUND, ce qui indique qu'il n'y a pas d'options de message pour le message en particulier.</span><span class="sxs-lookup"><span data-stu-id="4028e-115">The method always returns MAPI_E_NOT_FOUND, which indicates that there are no message options for the particular message.</span></span>
    
- <span data-ttu-id="4028e-116">**IMAPISession:: QueryDefaultMessageOpt**— les fournisseurs de services et clients MAPI ne doivent plus appeler cette méthode pour récupérer les propriétés qui contrôlent les options de message pour un type d'adresse particulier.</span><span class="sxs-lookup"><span data-stu-id="4028e-116">**IMAPISession::QueryDefaultMessageOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control message options for a particular address type.</span></span> <span data-ttu-id="4028e-117">La méthode ne renvoie plus un pointeur vers un tableau de valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="4028e-117">The method no longer returns a pointer to any array of property values.</span></span>
    
- <span data-ttu-id="4028e-118">**IAddrBook:: RecipOptions**: les fournisseurs de services et clients MAPI ne doivent plus appeler cette méthode pour afficher les propriétés ou permettre aux utilisateurs de définir des propriétés qui contrôlent le traitement pour un destinataire d'un type d'adresse particulier.</span><span class="sxs-lookup"><span data-stu-id="4028e-118">**IAddrBook::RecipOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control processing for a recipient of a particular address type.</span></span> <span data-ttu-id="4028e-119">La méthode renvoie toujours MAPI_W_ERRORS_RETURNED, ce qui indique qu'il n'y a pas d'options de destinataire pour le destinataire particulier.</span><span class="sxs-lookup"><span data-stu-id="4028e-119">The method always returns MAPI_W_ERRORS_RETURNED, which indicates that there are no recipient options for the particular recipient.</span></span>
    
- <span data-ttu-id="4028e-120">**IAddrBook:: QueryDefaultRecipOpt**— les fournisseurs de services et clients MAPI ne doivent plus appeler cette méthode pour récupérer les propriétés qui contrôlent les options de destinataire pour un type d'adresse particulier.</span><span class="sxs-lookup"><span data-stu-id="4028e-120">**IAddrBook::QueryDefaultRecipOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control recipient options for a particular address type.</span></span> <span data-ttu-id="4028e-121">La méthode ne renvoie plus un pointeur vers un tableau de valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="4028e-121">The method no longer returns a pointer to any array of property values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4028e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4028e-122">See also</span></span>



[<span data-ttu-id="4028e-123">Mise en route avec la référence de MAPI pour Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="4028e-123">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)

