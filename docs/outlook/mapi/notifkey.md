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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280046"
---
# <a name="notifkey"></a><span data-ttu-id="8fc75-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="8fc75-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="8fc75-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8fc75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8fc75-105">Identifie de manière unique une connexion entre un récepteur de notification, une source de notification et MAPI.</span><span class="sxs-lookup"><span data-stu-id="8fc75-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8fc75-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8fc75-106">Header file:</span></span>  <br/> |<span data-ttu-id="8fc75-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="8fc75-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="8fc75-108">Members</span><span class="sxs-lookup"><span data-stu-id="8fc75-108">Members</span></span>

 <span data-ttu-id="8fc75-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="8fc75-109">**cb**</span></span>
  
> <span data-ttu-id="8fc75-110">Nombre d'octets dans le membre **AB** .</span><span class="sxs-lookup"><span data-stu-id="8fc75-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="8fc75-111">**opér**</span><span class="sxs-lookup"><span data-stu-id="8fc75-111">**ab**</span></span>
  
> <span data-ttu-id="8fc75-112">Tableau d'octets qui décrivent la clé de notification.</span><span class="sxs-lookup"><span data-stu-id="8fc75-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8fc75-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="8fc75-113">Remarks</span></span>

<span data-ttu-id="8fc75-114">Les méthodes [subscribe](imapisupport-subscribe.md) et [Notify](imapisupport-notify.md) de [IMAPISupport](imapisupportiunknown.md) utilisent la structure **NOTIFKEY** pour générer des notifications au récepteur de notification approprié concernant la source de notification appropriée.</span><span class="sxs-lookup"><span data-stu-id="8fc75-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="8fc75-115">Les fournisseurs de services génèrent des clés de notification lorsque leur méthode de **Conseil** est appelée et qu'ils veulent appeler l' **abonnement** pour gérer l'inscription des notifications et l'envoi ultérieur de notifications.</span><span class="sxs-lookup"><span data-stu-id="8fc75-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="8fc75-116">Une clé de notification peut être l'identificateur d'entrée de la source de notification ou il peut s'agir d'un autre élément d'identification tel qu'une constante.</span><span class="sxs-lookup"><span data-stu-id="8fc75-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="8fc75-117">Par exemple, un fournisseur de banque de messages peut utiliser le chemin d'accès d'un dossier comme clé de notification.</span><span class="sxs-lookup"><span data-stu-id="8fc75-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="8fc75-118">La clé de notification doit fonctionner sur plusieurs processus.</span><span class="sxs-lookup"><span data-stu-id="8fc75-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="8fc75-119">Les exigences d'étendue pour une clé de notification ressemblent à celles d'un identificateur d'entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="8fc75-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="8fc75-120">Toutefois, contrairement à un identificateur d'entrée, une clé de notification doit être comparable au format binaire.</span><span class="sxs-lookup"><span data-stu-id="8fc75-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="8fc75-121">En règle générale, une clé de notification inclut une valeur **GUID** définie par le fournisseur de services, suivie d'autres informations propres au fournisseur, propres à l'objet.</span><span class="sxs-lookup"><span data-stu-id="8fc75-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="8fc75-122">Pour plus d'informations sur l'utilisation de la structure **NOTIFKEY** pour gérer les connexions entre les récepteurs de notification et les objets qui génèrent les notifications, consultez la rubrique [prise en charge](supporting-event-notification.md)de la notification d'événement.</span><span class="sxs-lookup"><span data-stu-id="8fc75-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8fc75-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fc75-123">See also</span></span>



[<span data-ttu-id="8fc75-124">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="8fc75-124">MAPI Structures</span></span>](mapi-structures.md)

