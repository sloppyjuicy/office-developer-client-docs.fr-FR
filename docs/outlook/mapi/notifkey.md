---
title: NOTIFKEY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFKEY
api_type:
- COM
ms.assetid: 031b7e18-59b2-445c-a747-348fda92f458
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429627"
---
# <a name="notifkey"></a><span data-ttu-id="33fc8-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="33fc8-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="33fc8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33fc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33fc8-105">Identifie de manière unique une connexion entre un sink de conseil, une source de conseil et MAPI.</span><span class="sxs-lookup"><span data-stu-id="33fc8-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33fc8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="33fc8-106">Header file:</span></span>  <br/> |<span data-ttu-id="33fc8-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="33fc8-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="33fc8-108">Members</span><span class="sxs-lookup"><span data-stu-id="33fc8-108">Members</span></span>

 <span data-ttu-id="33fc8-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="33fc8-109">**cb**</span></span>
  
> <span data-ttu-id="33fc8-110">Nombre d’octets dans le **membre ab.**</span><span class="sxs-lookup"><span data-stu-id="33fc8-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="33fc8-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="33fc8-111">**ab**</span></span>
  
> <span data-ttu-id="33fc8-112">Tableau d’octets décrivant la clé de notification.</span><span class="sxs-lookup"><span data-stu-id="33fc8-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="33fc8-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="33fc8-113">Remarks</span></span>

<span data-ttu-id="33fc8-114">Les [méthodes Subscribe](imapisupport-subscribe.md) et [Notify](imapisupport-notify.md) d’IMAPISupport utilisent la structure **NOTIFKEY** pour générer des notifications au réception de notifications approprié concernant la source de notification appropriée. [](imapisupportiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="33fc8-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="33fc8-115">Les fournisseurs de services génèrent des clés de notification lorsque leur méthode **Advise** est appelée et qu’ils souhaitent appeler **Subscribe** pour gérer l’inscription de la notification et l’envoi ultérieur de notifications.</span><span class="sxs-lookup"><span data-stu-id="33fc8-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="33fc8-116">Une clé de notification peut être l’identificateur d’entrée de la source de notification ou tout autre élément d’identification tel qu’une constante.</span><span class="sxs-lookup"><span data-stu-id="33fc8-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="33fc8-117">Par exemple, un fournisseur de magasins de messages peut utiliser le chemin d’accès d’un dossier comme clé de notification.</span><span class="sxs-lookup"><span data-stu-id="33fc8-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="33fc8-118">La clé de notification doit fonctionner sur plusieurs processus.</span><span class="sxs-lookup"><span data-stu-id="33fc8-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="33fc8-119">Les exigences d’étendue d’une clé de notification ressemblent à celles d’un identificateur d’entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="33fc8-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="33fc8-120">Toutefois, contrairement à un identificateur d’entrée, une clé de notification doit être comparable au binaire.</span><span class="sxs-lookup"><span data-stu-id="33fc8-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="33fc8-121">En règle générale, une clé de notification inclut une valeur **GUID** définie par le fournisseur de services, suivie d’autres informations spécifiques au fournisseur propres à l’objet.</span><span class="sxs-lookup"><span data-stu-id="33fc8-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="33fc8-122">Pour une discussion sur l’utilisation de la structure **NOTIFKEY** pour gérer les connexions entre les réceptions de notification et les objets qui génèrent les notifications, voir Notification d’événement de [prise en charge.](supporting-event-notification.md)</span><span class="sxs-lookup"><span data-stu-id="33fc8-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="33fc8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33fc8-123">See also</span></span>



[<span data-ttu-id="33fc8-124">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="33fc8-124">MAPI Structures</span></span>](mapi-structures.md)

