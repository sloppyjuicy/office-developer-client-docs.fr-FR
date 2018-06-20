---
title: Éléments d’API déconseillées dans cette version
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: c70e89efba585183d2019bbda49102ecd14b9e20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782922"
---
# <a name="api-elements-deprecated-in-this-edition"></a><span data-ttu-id="1929e-103">Éléments d’API déconseillées dans cette version</span><span class="sxs-lookup"><span data-stu-id="1929e-103">API Elements Deprecated in This Edition</span></span>

  
  
<span data-ttu-id="1929e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1929e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1929e-105">Éléments d’API suivants sont déconseillés dans Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="1929e-105">The following API elements are deprecated in Microsoft Outlook 2013.</span></span> <span data-ttu-id="1929e-106">Ils ne sont plus pris en charge et vous ne devez pas les utiliser dans les nouveaux projets.</span><span class="sxs-lookup"><span data-stu-id="1929e-106">They are no longer supported and you should not use them in new projects.</span></span>
  
## <a name="deprecation-of-message-and-recipient-options"></a><span data-ttu-id="1929e-107">Désapprobation de Message et des Options pour le destinataire</span><span class="sxs-lookup"><span data-stu-id="1929e-107">Deprecation of Message and Recipient Options</span></span>

<span data-ttu-id="1929e-108">Éléments d’API suivants sont déconseillés dans cette version, en raison de message obsolète et les options pour le destinataire :</span><span class="sxs-lookup"><span data-stu-id="1929e-108">The following API elements are deprecated in this release because of obsolete message and recipient options:</span></span>
  
- <span data-ttu-id="1929e-109">**IXPLogon::RegisterOptions**: sous-système MAPI appelle n’est plus cette méthode pour établir des valeurs par défaut pour les options de message et le destinataire d’un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="1929e-109">**IXPLogon::RegisterOptions**—The MAPI subsystem no longer calls this method to establish any default values for message and recipient options for a transport provider.</span></span>
    
- <span data-ttu-id="1929e-110">**OPTIONUTILITAIRE**— cette structure de données pris en charge des propriétés pour les options de message et le destinataire est obsolète.</span><span class="sxs-lookup"><span data-stu-id="1929e-110">**OPTIONDATA**—This data structure that supported properties for message and recipient options is obsolete.</span></span> <span data-ttu-id="1929e-111">Le sous-système MAPI appelle n’est plus **IXPLogon::RegisterOptions** pour obtenir un message ou une option de destinataire prend en charge par un fournisseur de transport pour un type particulier.</span><span class="sxs-lookup"><span data-stu-id="1929e-111">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** to obtain any message or recipient options that a transport provider supports for a particular address type.</span></span> 
    
- <span data-ttu-id="1929e-112">**OPTIONCALLBACK**— ce prototype de la fonction, un fournisseur de transport utilisé pour déclarer une fonction de rappel et qui, à son tour, le sous-système MAPI utilisé pour résoudre les propriétés du fournisseur, est obsolète.</span><span class="sxs-lookup"><span data-stu-id="1929e-112">**OPTIONCALLBACK**—This function prototype, which a transport provider used to declare a callback function and which, in turn, the MAPI subsystem used to resolve the provider's properties, is obsolete.</span></span> <span data-ttu-id="1929e-113">Le sous-système MAPI n’est plus appelle **IXPLogon::RegisterOptions** ou utilise une fonction de rappel retournée par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="1929e-113">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** or uses any callback function returned by the transport provider.</span></span> 
    
- <span data-ttu-id="1929e-114">**IMAPISession::MessageOptions**— les fournisseurs MAPI client et le service doivent appeler n’est plus de cette méthode pour afficher les propriétés ou permettre aux utilisateurs de définir les propriétés qui contrôlent un type particulier de message et l’adresse.</span><span class="sxs-lookup"><span data-stu-id="1929e-114">**IMAPISession::MessageOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control a particular message and address type.</span></span> <span data-ttu-id="1929e-115">La méthode renvoie toujours MAPI_E_NOT_FOUND, ce qui indique qu’il n’existe aucune option de message pour le message particulier.</span><span class="sxs-lookup"><span data-stu-id="1929e-115">The method always returns MAPI_E_NOT_FOUND, which indicates that there are no message options for the particular message.</span></span>
    
- <span data-ttu-id="1929e-116">**IMAPISession::QueryDefaultMessageOpt**— les fournisseurs MAPI client et le service doivent appeler n’est plus de cette méthode pour récupérer les propriétés qui contrôlent les options de messages pour un type particulier.</span><span class="sxs-lookup"><span data-stu-id="1929e-116">**IMAPISession::QueryDefaultMessageOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control message options for a particular address type.</span></span> <span data-ttu-id="1929e-117">N’est plus, la méthode renvoie un pointeur vers un tableau de valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="1929e-117">The method no longer returns a pointer to any array of property values.</span></span>
    
- <span data-ttu-id="1929e-118">**IAddrBook::RecipOptions**— les fournisseurs MAPI client et le service doivent appeler n’est plus de cette méthode pour afficher les propriétés ou permettre aux utilisateurs de définir les propriétés de contrôle du traitement d’un destinataire d’un type particulier.</span><span class="sxs-lookup"><span data-stu-id="1929e-118">**IAddrBook::RecipOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control processing for a recipient of a particular address type.</span></span> <span data-ttu-id="1929e-119">La méthode renvoie toujours MAPI_W_ERRORS_RETURNED, ce qui indique qu’il n’existe aucune option de destinataire pour le destinataire spécifique.</span><span class="sxs-lookup"><span data-stu-id="1929e-119">The method always returns MAPI_W_ERRORS_RETURNED, which indicates that there are no recipient options for the particular recipient.</span></span>
    
- <span data-ttu-id="1929e-120">**IAddrBook::QueryDefaultRecipOpt**— les fournisseurs MAPI client et le service doivent appeler n’est plus de cette méthode pour récupérer les propriétés qui contrôlent les options de destinataires pour un type particulier.</span><span class="sxs-lookup"><span data-stu-id="1929e-120">**IAddrBook::QueryDefaultRecipOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control recipient options for a particular address type.</span></span> <span data-ttu-id="1929e-121">N’est plus, la méthode renvoie un pointeur vers un tableau de valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="1929e-121">The method no longer returns a pointer to any array of property values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1929e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1929e-122">See also</span></span>



[<span data-ttu-id="1929e-123">Mise en route avec la r�f�rence de MAPI pour Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="1929e-123">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)

