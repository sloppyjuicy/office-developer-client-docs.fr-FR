---
title: Implémentation de l’Interface IClassFactory pour les serveurs de formulaire
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3ecae23d8631c818fb3d1c6786b2d180e9f32a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784198"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="04630-103">Implémentation de l’Interface IClassFactory pour les serveurs de formulaire</span><span class="sxs-lookup"><span data-stu-id="04630-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="04630-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="04630-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="04630-105">[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) est l’interface OLE qui utilisent des applications clientes pour créer des objets de formulaire de classe de message du serveur de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="04630-105">[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="04630-106">Le tableau suivant répertorie les méthodes **IClassFactory** qui sont requis.</span><span class="sxs-lookup"><span data-stu-id="04630-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="04630-107">**Méthode**</span><span class="sxs-lookup"><span data-stu-id="04630-107">**Method**</span></span>|<span data-ttu-id="04630-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="04630-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04630-109">CreateInstance</span><span class="sxs-lookup"><span data-stu-id="04630-109">CreateInstance</span></span>](http://msdn.microsoft.com/en-us/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="04630-110">Crée un nouvel objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="04630-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="04630-111">LockServer</span><span class="sxs-lookup"><span data-stu-id="04630-111">LockServer</span></span>](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="04630-112">Verrouille le serveur de formulaire en mémoire afin que la surcharge de démarrage peut être évité lorsque plusieurs objets de formulaire sont créés.</span><span class="sxs-lookup"><span data-stu-id="04630-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="04630-113">Pour toutes les informations nécessaires pour implémenter ces méthodes, voir la section COM et ActiveX Object Services dans le SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="04630-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="04630-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04630-114">See also</span></span>



[<span data-ttu-id="04630-115">Écriture de Code de formulaire Server</span><span class="sxs-lookup"><span data-stu-id="04630-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

