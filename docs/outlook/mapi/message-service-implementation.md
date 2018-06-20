---
title: Mise en œuvre de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6ba2f9542fd021c544d73d8208ed356a7bf95309
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784881"
---
# <a name="message-service-implementation"></a><span data-ttu-id="1055c-103">Mise en œuvre de message</span><span class="sxs-lookup"><span data-stu-id="1055c-103">Message Service Implementation</span></span>

  
  
<span data-ttu-id="1055c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1055c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1055c-105">Un service de message est un ou plusieurs fournisseurs de services connexes regroupés en vue de simplifier l’installation et la configuration.</span><span class="sxs-lookup"><span data-stu-id="1055c-105">A message service is one or more related service providers grouped together for the purpose of simplifying installation and configuration.</span></span> <span data-ttu-id="1055c-106">Tous les fournisseurs de services doivent être inclus dans un service de message.</span><span class="sxs-lookup"><span data-stu-id="1055c-106">All service providers should be included in a message service.</span></span>
  
<span data-ttu-id="1055c-107">Pour implémenter un service de message avec un ou plusieurs fournisseurs, utilisez la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="1055c-107">To implement a message service with one or more providers, use the following procedure:</span></span>
  
1. <span data-ttu-id="1055c-108">Conception du service de message, déterminer le nombre et le type de fournisseurs de services à inclure.</span><span class="sxs-lookup"><span data-stu-id="1055c-108">Design the message service, determining the number and type of service providers to be included.</span></span> <span data-ttu-id="1055c-109">Pour plus d’informations sur la conception d’un service de message, consultez [conception d’un Service de Message](designing-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="1055c-109">For more information about how to design a message service, see [Designing a Message Service](designing-a-message-service.md).</span></span>
    
2. <span data-ttu-id="1055c-110">Créer un programme d’installation pour installer les fournisseurs de services dans le service de message.</span><span class="sxs-lookup"><span data-stu-id="1055c-110">Create a setup program to install the service providers in the message service.</span></span> <span data-ttu-id="1055c-111">Pour plus d’informations sur l’écriture d’un programme d’installation du service message, consultez [Installation du Service de Message prise en charge](supporting-message-service-installation.md).</span><span class="sxs-lookup"><span data-stu-id="1055c-111">For more information about writing a message service setup program, see [Supporting Message Service Installation](supporting-message-service-installation.md).</span></span> 
    
3. <span data-ttu-id="1055c-112">Créez une fonction de point d’entrée pour effectuer une configuration.</span><span class="sxs-lookup"><span data-stu-id="1055c-112">Create an entry point function to perform configuration.</span></span> <span data-ttu-id="1055c-113">Pour plus d’informations sur l’écriture d’une entrée de service de message point fonction, voir [Configuration du Service de Message prise en charge](supporting-message-service-configuration.md) et [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="1055c-113">For more information about writing a message service entry point function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span></span> 
    
4. <span data-ttu-id="1055c-114">Créez un fichier d’en-tête public qui contient des descriptions des valeurs valides pour les propriétés personnalisées que le service prend en charge les balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="1055c-114">Create a public header file that contains the property tags and descriptions of valid values for any custom properties that the message service supports.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1055c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1055c-115">See also</span></span>



[<span data-ttu-id="1055c-116">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="1055c-116">MAPI Service Providers</span></span>](mapi-service-providers.md)

