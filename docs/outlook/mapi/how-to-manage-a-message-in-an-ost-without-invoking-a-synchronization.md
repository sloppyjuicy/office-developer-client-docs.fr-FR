---
title: Gérer les messages en mode OST sans avoir à invoquer une synchronisation en mode Exchange mis en cache
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Contient un exemple de code en C++ qui montre comment utiliser IID_IMessageRaw dans IMsgStore::OpenEntry pour obtenir une interface IMessage qui gère un message dans un fichier de dossiers hors connexion (OST) sans forcer le téléchargement de l’intégralité du message lorsque le client est en mode Exchange mis en cache.
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418756"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="f1a23-103">Gérer les messages en mode OST sans avoir à invoquer une synchronisation en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="f1a23-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="f1a23-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1a23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1a23-105">Cette rubrique contient un exemple de code en C++ qui montre comment utiliser `IID_IMessageRaw` **[IMsgStore::OpenEntry](imsgstore-openentry.md)** pour obtenir une interface **[IMessage](imessageimapiprop.md)** qui gère un message dans un fichier de dossiers hors connexion (OST) sans forcer le téléchargement de l’intégralité du message lorsque le client est en mode Exchange mis en cache.</span><span class="sxs-lookup"><span data-stu-id="f1a23-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="f1a23-106">Lorsqu’un client est en mode Exchange mis en cache, les messages en mode OST peuvent être dans l’un des deux états :</span><span class="sxs-lookup"><span data-stu-id="f1a23-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="f1a23-107">Le message entier qui contient l’en-tête et le corps est téléchargé.</span><span class="sxs-lookup"><span data-stu-id="f1a23-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="f1a23-108">Le message avec uniquement son en-tête est téléchargé.</span><span class="sxs-lookup"><span data-stu-id="f1a23-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="f1a23-109">Lorsque vous demandez une interface **IMessage** pour un message dans un OST et que le client est en mode Exchange mis en cache, utilisez `IID_IMessageRaw` .</span><span class="sxs-lookup"><span data-stu-id="f1a23-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="f1a23-110">Si vous demandez une  `IID_IMessage` interface **IMessage** et que seul son en-tête est téléchargé dans le système OST, vous devez appeler une synchronisation qui tente de télécharger l’intégralité du message.</span><span class="sxs-lookup"><span data-stu-id="f1a23-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="f1a23-111">Si vous utilisez  `IID_IMessageRaw` ou demandez une interface  `IID_IMessage` **IMessage,** les interfaces renvoyées sont en cours d’utilisation identiques.</span><span class="sxs-lookup"><span data-stu-id="f1a23-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="f1a23-112">**L’interface IMessage** qui a été demandée à l’aide renvoie un message électronique tel qu’il existe dans le OST, et la `IID_IMessageRaw` synchronisation n’est pas forcée.</span><span class="sxs-lookup"><span data-stu-id="f1a23-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="f1a23-113">L’exemple suivant montre comment appeler la **méthode OpenEntry,** en passant  `IID_IMessageRaw` au lieu de  `IID_IMessage` .</span><span class="sxs-lookup"><span data-stu-id="f1a23-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
```cpp
HRESULT HrOpenRawMessage ( 
    LPMDB lpMSB,  
    ULONG cbEntryID,  
    LPENTRYID lpEntryID,  
    ULONG ulFlags,  
    LPMESSAGE* lpMessage) 
{ 
    ULONG ulObjType = NULL; 
 
    HRESULT hRes = lpMDB->OpenEntry( 
        cbEntryID, 
        lpEntryID, 
        IID_IMessageRaw, 
        ulFlags, 
        &ulObjType, 
        (LPUNKNOWN*) lpMessage)); 
 
   return hRes; 
} 

```

<span data-ttu-id="f1a23-114">Si la **méthode OpenEntry** renvoie le code **d’MAPI_E_INTERFACE_NOT_SUPPORTED,** elle indique que la boutique de messages ne prend pas en charge l’accès au message en mode brut.</span><span class="sxs-lookup"><span data-stu-id="f1a23-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="f1a23-115">Dans ce cas, essayez à nouveau **la méthode OpenEntry** en passant  `IID_IMessage` .</span><span class="sxs-lookup"><span data-stu-id="f1a23-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="f1a23-116">`IID_IMessageRaw` peut ne pas être défini dans le fichier d’en-tête téléchargeable dont vous disposez actuellement.</span><span class="sxs-lookup"><span data-stu-id="f1a23-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="f1a23-117">Dans ce cas, vous pouvez l’ajouter à votre code à l’aide de la définition suivante.</span><span class="sxs-lookup"><span data-stu-id="f1a23-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="f1a23-118">Utilisez la macro DEFINE_OLEGUID définie dans le fichier d’en-tête guiddef.h du Kit de développement logiciel (SDK) Microsoft Windows pour associer le nom symbolique GUID à sa valeur.</span><span class="sxs-lookup"><span data-stu-id="f1a23-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="f1a23-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1a23-119">See also</span></span>

- [<span data-ttu-id="f1a23-120">À propos des ajouts MAPI</span><span class="sxs-lookup"><span data-stu-id="f1a23-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="f1a23-121">Accès à une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="f1a23-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="f1a23-122">Ouvrir une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="f1a23-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

