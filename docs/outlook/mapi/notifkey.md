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
ms.openlocfilehash: 3c480c420753b2da6c57b3961589d5c2e2e8022a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784921"
---
# <a name="notifkey"></a><span data-ttu-id="44df6-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="44df6-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="44df6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44df6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44df6-105">Identifie de manière unique une connexion entre un récepteur de notifications, une source de notifications et MAPI.</span><span class="sxs-lookup"><span data-stu-id="44df6-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44df6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="44df6-106">Header file:</span></span>  <br/> |<span data-ttu-id="44df6-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="44df6-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="44df6-108">Membres</span><span class="sxs-lookup"><span data-stu-id="44df6-108">Members</span></span>

 <span data-ttu-id="44df6-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="44df6-109">**cb**</span></span>
  
> <span data-ttu-id="44df6-110">Nombre d’octets dans le membre de **Carnet d’adresses** .</span><span class="sxs-lookup"><span data-stu-id="44df6-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="44df6-111">**Carnet d’adresses**</span><span class="sxs-lookup"><span data-stu-id="44df6-111">**ab**</span></span>
  
> <span data-ttu-id="44df6-112">Tableau d’octets décrivant la clé de notification.</span><span class="sxs-lookup"><span data-stu-id="44df6-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44df6-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="44df6-113">Remarks</span></span>

<span data-ttu-id="44df6-114">Les méthodes [Subscribe](imapisupport-subscribe.md) et [notifier](imapisupport-notify.md) de [IMAPISupport](imapisupportiunknown.md) permet de générer des notifications pour le récepteur de notifications appropriées sur la source advise appropriée la structure **NOTIFKEY** .</span><span class="sxs-lookup"><span data-stu-id="44df6-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="44df6-115">Fournisseurs de services de génèrent des clés de notification lorsque leur méthode **Advise** est appelée et qu’ils souhaitent **s’abonner** pour gérer l’inscription de notification et l’envoi suivants de notifications d’appel.</span><span class="sxs-lookup"><span data-stu-id="44df6-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="44df6-116">Une clé de notification peut être l’identificateur d’entrée de la source advise ou elle peut être n’importe quel autre élément identification comme une constante.</span><span class="sxs-lookup"><span data-stu-id="44df6-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="44df6-117">Par exemple, un fournisseur de magasin de message peut utiliser le chemin d’accès d’un dossier en tant que sa clé de notification.</span><span class="sxs-lookup"><span data-stu-id="44df6-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="44df6-118">La clé de notification devrait fonctionner sur plusieurs processus.</span><span class="sxs-lookup"><span data-stu-id="44df6-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="44df6-119">Les exigences de l’étendue d’une clé de notification ressemblent à celles d’un identificateur d’entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="44df6-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="44df6-120">Toutefois, contrairement à un identificateur d’entrée, une clé de notification doit être binaire comparable.</span><span class="sxs-lookup"><span data-stu-id="44df6-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="44df6-121">En règle générale, une clé de notification inclut une valeur **GUID** définie par le fournisseur de suivi d’autres informations spécifiques au fournisseur uniques à l’objet.</span><span class="sxs-lookup"><span data-stu-id="44df6-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="44df6-122">Pour une description de l’utilisation de la structure **NOTIFKEY** pour gérer les connexions entre les récepteurs de notifications et les objets qui génèrent des notifications, voir [Prise en charge de Notification d’événement](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="44df6-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44df6-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44df6-123">See also</span></span>



[<span data-ttu-id="44df6-124">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="44df6-124">MAPI Structures</span></span>](mapi-structures.md)

