---
title: Publication du fournisseur de transport
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: ea9656f9571777478d3db9a2613fbff5ddef0ee6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592289"
---
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="66199-103">Publication du fournisseur de transport</span><span class="sxs-lookup"><span data-stu-id="66199-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="66199-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66199-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66199-105">Lorsque MAPI ou le spouleur MAPI est terminée à l’aide d’un objet de connexion de transport :</span><span class="sxs-lookup"><span data-stu-id="66199-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="66199-106">MAPI ou le spouleur MAPI appelle la méthode de [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="66199-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="66199-107">Le fournisseur de transport invalide l’objet d’état en appelant la méthode [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) .</span><span class="sxs-lookup"><span data-stu-id="66199-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="66199-108">Si le fournisseur de transport invalide les objets de message sont envoyées ou reçues au moment de l’appel **TransportLogoff** varie selon les indicateurs qui ont été transmis à **TransportLogoff**.</span><span class="sxs-lookup"><span data-stu-id="66199-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="66199-109">Le fournisseur de transport appelle la méthode [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de l’objet de la prise en charge pour supprimer la ligne du fournisseur de transport à partir de la table d’état et de supprimer des tables internes des identificateurs uniques (UID) qui ont été définies avec la [IMAPISupport :: SetProviderUID](imapisupport-setprovideruid.md) méthode.</span><span class="sxs-lookup"><span data-stu-id="66199-109">The transport provider calls the support object's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="66199-110">Il décrémente le nombre d’objets connus d’ouverture de session actives sur cet objet fournisseur.</span><span class="sxs-lookup"><span data-stu-id="66199-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="66199-111">Si le nombre est égal à zéro, MAPI appelle la méthode [IXPProvider::Shutdown](ixpprovider-shutdown.md) et la **version** de l’objet fournisseur.</span><span class="sxs-lookup"><span data-stu-id="66199-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="66199-112">S’il s’agissait du dernier objet connus fournisseur à l’aide de cette DLL sur ce processus, MAPI appelle la fonction **FreeLibrary** sur la DLL à une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="66199-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="66199-113">La mémoire pour l’objet de prise en charge MAPI est libérée et renvoie l’objet de prise en charge de méthode de **publication** .</span><span class="sxs-lookup"><span data-stu-id="66199-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="66199-114">La méthode **TransportLogoff** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="66199-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="66199-115">MAPI ou le spouleur MAPI appelle **Release** sur un objet de connexion du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="66199-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="66199-116">La mémoire pour l’objet est publiée.</span><span class="sxs-lookup"><span data-stu-id="66199-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="66199-117">MAPI ou le spouleur MAPI appelle **FreeLibrary** sur la DLL du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="66199-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="66199-118">Pour robustesse, les objets d’ouverture de session et le fournisseur doivent être en mesure de gérer les appels **version** finales sur eux-mêmes sans avoir leur **TransportLogoff** ou les méthodes de **l’arrêt de** l’appelé.</span><span class="sxs-lookup"><span data-stu-id="66199-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="66199-119">Si la **version** est appelée dans ce cas, les fournisseurs de transport doivent traiter les appels comme **TransportLogoff** ou **l’arrêt** avait été appelée avec un zéro argument, suivi de **version**.</span><span class="sxs-lookup"><span data-stu-id="66199-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

