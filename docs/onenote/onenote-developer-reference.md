---
title: Référence du développeur OneNote
manager: soliver
ms.date: 05/16/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4c4ef9e8-6b30-481b-8023-2e1280bcbcc9
description: Cette référence contient des présentations conceptuelles et références de programmation pour vous aider à développer des solutions pour les applications de client de bureau OneNote 2013.
ms.openlocfilehash: b19e9957d1faed1bda150df34f61209d9f40fc5d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395706"
---
# <a name="onenote-developer-reference"></a><span data-ttu-id="13e98-103">Référence du développeur OneNote</span><span class="sxs-lookup"><span data-stu-id="13e98-103">OneNote developer reference</span></span>

<span data-ttu-id="13e98-104">Cette référence contient des présentations conceptuelles et références de programmation pour vous aider à développer des solutions pour les applications de client de bureau OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="13e98-104">This reference contains conceptual overviews and programmatic references to guide you in developing solutions for OneNote 2013 desktop client applications.</span></span> <span data-ttu-id="13e98-105">Il inclut tous les ajouts et modifications à l’interface de programmation d’application (API) de OneNote 2013 et fournit des exemples de code en c#, montre comment effectuer des tâches dans OneNote.</span><span class="sxs-lookup"><span data-stu-id="13e98-105">It includes all the additions and changes to the OneNote 2013 application programming interface (API), and provides code samples in C# to show how to perform some tasks in OneNote.</span></span> <span data-ttu-id="13e98-106">L’API de 2013 OneNote permet aux utilisateurs d’accéder par programme et modifier le contenu de OneNote.</span><span class="sxs-lookup"><span data-stu-id="13e98-106">The OneNote 2013 API enables users to programmatically access and edit OneNote content.</span></span> <span data-ttu-id="13e98-107">Les utilisateurs peuvent également apporter des modifications à l’affichage des fenêtres OneNote.</span><span class="sxs-lookup"><span data-stu-id="13e98-107">Users can also make changes to the view of OneNote windows.</span></span>
  
<span data-ttu-id="13e98-108">Cette documentation contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="13e98-108">This documentation contains the following information:</span></span>
  
- <span data-ttu-id="13e98-109">[Interfaces de fenêtre](window-interfaces-onenote.md): décrit les interfaces de **fenêtre** et **Windows** , qui permettent aux utilisateurs d’énumérer l’ensemble des fenêtres OneNote et de modifier certaines propriétés de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="13e98-109">[Window interfaces](window-interfaces-onenote.md): Describes the **Window** and **Windows** interfaces, which enable users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
    
- <span data-ttu-id="13e98-110">[Interfaces de boîte de dialogue classement rapide](quick-filing-dialog-box-interfaces-onenote.md): décrit les interfaces que vous pouvez utiliser pour personnaliser par programme la boîte de dialogue **Classement rapide** de OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="13e98-110">[Quick Filing dialog box interfaces](quick-filing-dialog-box-interfaces-onenote.md): Describes the interfaces that you can use to programmatically customize the **Quick Filing** dialog box in OneNote 2013.</span></span> 
    
- <span data-ttu-id="13e98-111">[Interface de l’application](application-interface-onenote.md): décrit les méthodes, propriétés et événements qui vous permettent de récupérer, manipuler et mettre à jour les informations de OneNote 2013 et le contenu.</span><span class="sxs-lookup"><span data-stu-id="13e98-111">[Application interface](application-interface-onenote.md): Describes methods, properties, and events that help retrieve, manipulate, and update OneNote 2013 information and content.</span></span>
    
- <span data-ttu-id="13e98-112">[Énumérations](enumerations-onenote-developer-reference.md): décrit les énumérations dans le modèle d’objet OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="13e98-112">[Enumerations](enumerations-onenote-developer-reference.md): Describes the enumerations in the OneNote 2013 object model.</span></span>
    
- <span data-ttu-id="13e98-113">[Codes d’erreur](error-codes-onenote.md): répertorie les codes d’erreur dans le modèle d’objet OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="13e98-113">[Error codes](error-codes-onenote.md): Lists the error codes in the OneNote 2013 object model.</span></span>
    
> [!NOTE]
> <span data-ttu-id="13e98-p102">Les API décrites dans cette documentation sont conçues uniquement pour les solutions clientes de bureau Win32 OneNote dans les scénarios sans connexion. Pour les scénarios avec connexion, utilisez les API du service OneNote recommandées. Pour plus d'informations, consultez le site [dev.onenote.com](https://go.microsoft.com/fwlink/?LinkID=390615).</span><span class="sxs-lookup"><span data-stu-id="13e98-p102">The APIs described in this documentation are intended only for OneNote Win32 desktop client solutions in unconnected scenarios. For connected scenarios, use the recommended OneNote service APIs. To learn more, visit [dev.onenote.com](https://go.microsoft.com/fwlink/?LinkID=390615).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="13e98-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13e98-117">See also</span></span>

- [<span data-ttu-id="13e98-118">OneNote pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="13e98-118">OneNote for developers</span></span>](https://go.microsoft.com/fwlink/?LinkID=390615)   
- <span data-ttu-id="13e98-119">[Exemples de référentiels](https://github.com/OneNoteDev/) (OneNote service API)</span><span class="sxs-lookup"><span data-stu-id="13e98-119">[Samples on GitHub](https://github.com/OneNoteDev/) (OneNote service APIs)</span></span>     
- [<span data-ttu-id="13e98-120">Accessibilité des produits Microsoft</span><span class="sxs-lookup"><span data-stu-id="13e98-120">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)    
- [<span data-ttu-id="13e98-121">Conventions de document</span><span class="sxs-lookup"><span data-stu-id="13e98-121">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)    
- [<span data-ttu-id="13e98-122">Informations de Copyright de référence pour développeur OneNote</span><span class="sxs-lookup"><span data-stu-id="13e98-122">OneNote Developer Reference Copyright Information</span></span>](https://msdn.microsoft.com/library/office/jj680116.aspx)
    
    

