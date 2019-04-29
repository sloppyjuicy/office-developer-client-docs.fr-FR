---
title: Implémentation du service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ef3820afbd4ae7ff04a3f54071e56f4e0a856109
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434031"
---
# <a name="message-service-implementation"></a><span data-ttu-id="15171-103">Implémentation du service de messagerie</span><span class="sxs-lookup"><span data-stu-id="15171-103">Message Service Implementation</span></span>

  
  
<span data-ttu-id="15171-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15171-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15171-105">Un service de messagerie est un ou plusieurs fournisseurs de services associés pour simplifier l'installation et la configuration.</span><span class="sxs-lookup"><span data-stu-id="15171-105">A message service is one or more related service providers grouped together for the purpose of simplifying installation and configuration.</span></span> <span data-ttu-id="15171-106">Tous les fournisseurs de services doivent être inclus dans un service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="15171-106">All service providers should be included in a message service.</span></span>
  
<span data-ttu-id="15171-107">Pour implémenter un service de messagerie avec un ou plusieurs fournisseurs, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="15171-107">To implement a message service with one or more providers, use the following procedure:</span></span>
  
1. <span data-ttu-id="15171-108">Concevez le service de messagerie en déterminant le nombre et le type de fournisseurs de services à inclure.</span><span class="sxs-lookup"><span data-stu-id="15171-108">Design the message service, determining the number and type of service providers to be included.</span></span> <span data-ttu-id="15171-109">Pour plus d'informations sur la création d'un service de messagerie, consultez la rubrique [conception d'un service de messagerie](designing-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="15171-109">For more information about how to design a message service, see [Designing a Message Service](designing-a-message-service.md).</span></span>
    
2. <span data-ttu-id="15171-110">Créez un programme d'installation pour installer les fournisseurs de services dans le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="15171-110">Create a setup program to install the service providers in the message service.</span></span> <span data-ttu-id="15171-111">Pour plus d'informations sur l'écriture d'un programme d'installation du service de messagerie, consultez la rubrique [supportIng message service installation](supporting-message-service-installation.md).</span><span class="sxs-lookup"><span data-stu-id="15171-111">For more information about writing a message service setup program, see [Supporting Message Service Installation](supporting-message-service-installation.md).</span></span> 
    
3. <span data-ttu-id="15171-112">Créez une fonction de point d'entrée pour effectuer la configuration.</span><span class="sxs-lookup"><span data-stu-id="15171-112">Create an entry point function to perform configuration.</span></span> <span data-ttu-id="15171-113">Pour plus d'informations sur l'écriture d'une fonction de point d'entrée de service de messagerie, voir [supportIng Configuration service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="15171-113">For more information about writing a message service entry point function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span></span> 
    
4. <span data-ttu-id="15171-114">Créez un fichier d'en-tête public contenant les balises de propriété et des descriptions des valeurs valides pour toutes les propriétés personnalisées prises en charge par le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="15171-114">Create a public header file that contains the property tags and descriptions of valid values for any custom properties that the message service supports.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="15171-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15171-115">See also</span></span>



[<span data-ttu-id="15171-116">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="15171-116">MAPI Service Providers</span></span>](mapi-service-providers.md)

