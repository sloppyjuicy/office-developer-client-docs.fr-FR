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
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328384"
---
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="27555-103">Publication du fournisseur de transport</span><span class="sxs-lookup"><span data-stu-id="27555-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="27555-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27555-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27555-105">Lorsque MAPI ou le spouleur MAPI se termine à l'aide d'un objet de connexion de transport:</span><span class="sxs-lookup"><span data-stu-id="27555-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="27555-106">MAPI ou le spouleur MAPI appelle la méthode [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="27555-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="27555-107">Le fournisseur de transport annule l'objet d'État en appelant la méthode [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) .</span><span class="sxs-lookup"><span data-stu-id="27555-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="27555-108">Le fait que le fournisseur de transport invalide ou non les objets de message envoyés ou reçus au moment de l'appel **TransportLogoff** dépend des indicateurs transmis à **TransportLogoff**.</span><span class="sxs-lookup"><span data-stu-id="27555-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="27555-109">Le fournisseur de transport appelle la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de l'objet de prise en charge pour supprimer la ligne du fournisseur de transport de la table d'État et supprimer des tables internes les identificateurs uniques (UID) qui ont été définis avec l' [IMAPISupport:: Méthode SetProviderUID](imapisupport-setprovideruid.md) .</span><span class="sxs-lookup"><span data-stu-id="27555-109">The transport provider calls the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="27555-110">Il décrémente le nombre d'objets d'ouverture de session connus actifs sur cet objet fournisseur.</span><span class="sxs-lookup"><span data-stu-id="27555-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="27555-111">Si le nombre atteint zéro, MAPI appelle la méthode [IXPProvider:: Shutdown](ixpprovider-shutdown.md) et la **libération** sur l'objet fournisseur.</span><span class="sxs-lookup"><span data-stu-id="27555-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="27555-112">S'il s'agissait du dernier objet fournisseur connu utilisant cette DLL lors de ce processus, MAPI appelle la fonction **FreeLibrary** sur la dll ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="27555-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="27555-113">La mémoire de l'objet de prise en charge MAPI est libérée et la méthode de **libération** d'objet de prise en charge est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="27555-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="27555-114">La méthode **TransportLogoff** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="27555-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="27555-115">MAPI ou le spouleur MAPI appelle la **version** de l'objet de connexion du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="27555-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="27555-116">La mémoire de l'objet est libérée.</span><span class="sxs-lookup"><span data-stu-id="27555-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="27555-117">MAPI ou le spouleur MAPI appelle **FreeLibrary** sur la dll du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="27555-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="27555-118">Pour des méthodes de robustesse, les objets Logon et Provider doivent être en mesure de gérer eux-mêmes les appels de la **version** finale sans avoir préalablement appelé leurs méthodes **TransportLogoff** ou **Shutdown** .</span><span class="sxs-lookup"><span data-stu-id="27555-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="27555-119">Si **Release** est appelé dans ce cas, les fournisseurs de transport doivent traiter les appels comme si **TransportLogoff** ou **Shutdown** avait été appelé avec un argument zéro suivi de **Release**.</span><span class="sxs-lookup"><span data-stu-id="27555-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

