---
title: Implémentation de l'interface IClassFactory pour les serveurs de formulaires
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310030"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="1052b-103">Implémentation de l'interface IClassFactory pour les serveurs de formulaires</span><span class="sxs-lookup"><span data-stu-id="1052b-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="1052b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1052b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1052b-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) est l'interface OLE utilisée par les applications clientes pour créer de nouveaux objets Form de la classe de message de votre serveur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="1052b-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="1052b-106">Le tableau suivant répertorie les méthodes **IClassFactory** requises.</span><span class="sxs-lookup"><span data-stu-id="1052b-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="1052b-107">**Méthode**</span><span class="sxs-lookup"><span data-stu-id="1052b-107">**Method**</span></span>|<span data-ttu-id="1052b-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="1052b-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1052b-109">CreateInstance</span><span class="sxs-lookup"><span data-stu-id="1052b-109">CreateInstance</span></span>](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="1052b-110">Crée un nouvel objet Form.</span><span class="sxs-lookup"><span data-stu-id="1052b-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="1052b-111">LockServer</span><span class="sxs-lookup"><span data-stu-id="1052b-111">LockServer</span></span>](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="1052b-112">Verrouille le serveur de formulaires en mémoire afin que la charge de démarrage puisse être évitée lors de la création d'objets de formulaire.</span><span class="sxs-lookup"><span data-stu-id="1052b-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="1052b-113">Pour obtenir toutes les informations nécessaires à l'implémentation de ces méthodes, voir la section COM and ActiveX Object Services dans le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="1052b-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1052b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1052b-114">See also</span></span>



[<span data-ttu-id="1052b-115">Écriture de code de serveur de formulaire</span><span class="sxs-lookup"><span data-stu-id="1052b-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

