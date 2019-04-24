---
title: Référence du développeur OneNote
manager: soliver
ms.date: 05/16/2016
ms.audience: Developer
ms.assetid: 4c4ef9e8-6b30-481b-8023-2e1280bcbcc9
description: Cette référence contient des présentations conceptuelles et des références programmatiques qui vous guideront tout au long du développement de solutions dédiées aux applications clientes de bureau OneNote 2013.
localization_priority: Priority
ms.openlocfilehash: d2b401a768e62c4b9712b1590bfaf499c2b022ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317051"
---
# <a name="onenote-developer-reference"></a><span data-ttu-id="07cbc-103">Référence du développeur OneNote</span><span class="sxs-lookup"><span data-stu-id="07cbc-103">OneNote developer reference</span></span>

<span data-ttu-id="07cbc-104">Cette référence contient des présentations conceptuelles et des références programmatiques qui vous guideront tout au long du développement de solutions dédiées aux applications clientes de bureau OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="07cbc-104">This reference contains conceptual overviews and programmatic references to guide you in developing solutions for OneNote 2013 desktop client applications.</span></span> <span data-ttu-id="07cbc-105">Elle inclut tous les ajouts et modifications apportés à l’interface de programmation d’application (API) OneNote 2013, et fournit des exemples de code dans C# pour montrer comment effectuer certaines tâches dans OneNote.</span><span class="sxs-lookup"><span data-stu-id="07cbc-105">It includes all the additions and changes to the OneNote 2013 application programming interface (API), and provides code samples in C# to show how to perform some tasks in OneNote.</span></span> <span data-ttu-id="07cbc-106">L’API OneNote 2013 permet aux utilisateurs d’accéder à OneNote par programme et d’en modifier le contenu.</span><span class="sxs-lookup"><span data-stu-id="07cbc-106">The OneNote 2013 API enables users to programmatically access and edit OneNote content.</span></span> <span data-ttu-id="07cbc-107">Les utilisateurs peuvent également apporter des modifications à l’affichage des fenêtres OneNote.</span><span class="sxs-lookup"><span data-stu-id="07cbc-107">Users can also make changes to the view of OneNote windows.</span></span>
  
<span data-ttu-id="07cbc-108">Cette documentation contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="07cbc-108">This documentation contains the following information:</span></span>
  
- <span data-ttu-id="07cbc-109">[Interfaces de fenêtres](window-interfaces-onenote.md) : décrit les interfaces **Fenêtre** et **Fenêtres** qui permettent aux utilisateurs de dénombrer les différentes fenêtres OneNote et d’en modifier certaines des propriétés.</span><span class="sxs-lookup"><span data-stu-id="07cbc-109">[Window interfaces](window-interfaces-onenote.md): Describes the **Window** and **Windows** interfaces, which enable users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
    
- <span data-ttu-id="07cbc-110">[Interfaces de boîtes de dialogue Remplissage rapide](quick-filing-dialog-box-interfaces-onenote.md) : décrit les interfaces que vous pouvez utiliser pour personnaliser par programme la boîte de dialogue **Remplissage rapide** dans OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="07cbc-110">[Quick Filing dialog box interfaces](quick-filing-dialog-box-interfaces-onenote.md): Describes the interfaces that you can use to programmatically customize the **Quick Filing** dialog box in OneNote 2013.</span></span> 
    
- <span data-ttu-id="07cbc-111">[Interface d’applications](application-interface-onenote.md) : décrit les méthodes, les propriétés et les événements qui vous aident à récupérer, à manipuler et à mettre à jour les informations et le contenu de OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="07cbc-111">[Application interface](application-interface-onenote.md): Describes methods, properties, and events that help retrieve, manipulate, and update OneNote 2013 information and content.</span></span>
    
- <span data-ttu-id="07cbc-112">[Énumérations](enumerations-onenote-developer-reference.md) : décrit les énumérations dans le modèle objet OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="07cbc-112">[Enumerations](enumerations-onenote-developer-reference.md): Describes the enumerations in the OneNote 2013 object model.</span></span>
    
- <span data-ttu-id="07cbc-113">[Codes d’erreur](error-codes-onenote.md) : répertorie les codes d’erreur dans le modèle objet OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="07cbc-113">[Error codes](error-codes-onenote.md): Lists the error codes in the OneNote 2013 object model.</span></span>
    
> [!NOTE]
> <span data-ttu-id="07cbc-p102">Les API décrites dans cette documentation sont conçues uniquement pour les solutions clientes de bureau Win32 OneNote dans les scénarios sans connexion. Pour les scénarios avec connexion, utilisez les API du service OneNote recommandées. Pour plus d'informations, consultez le site [dev.onenote.com](https://go.microsoft.com/fwlink/?LinkID=390615).</span><span class="sxs-lookup"><span data-stu-id="07cbc-p102">The APIs described in this documentation are intended only for OneNote Win32 desktop client solutions in unconnected scenarios. For connected scenarios, use the recommended OneNote service APIs. To learn more, visit [dev.onenote.com](https://go.microsoft.com/fwlink/?LinkID=390615).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="07cbc-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07cbc-117">See also</span></span>

- [<span data-ttu-id="07cbc-118">OneNote pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="07cbc-118">OneNote for developers</span></span>](https://go.microsoft.com/fwlink/?LinkID=390615)   
- <span data-ttu-id="07cbc-119">[Échantillons sur GitHub](https://github.com/OneNoteDev/) (API du service OneNote)</span><span class="sxs-lookup"><span data-stu-id="07cbc-119">[Samples on GitHub](https://github.com/OneNoteDev/) (OneNote service APIs)</span></span>     
- [<span data-ttu-id="07cbc-120">Accessibilité des produits Microsoft</span><span class="sxs-lookup"><span data-stu-id="07cbc-120">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)    
- [<span data-ttu-id="07cbc-121">Conventions de document</span><span class="sxs-lookup"><span data-stu-id="07cbc-121">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)    
- [<span data-ttu-id="07cbc-122">Informations de copyright de référence du développeur OneNote</span><span class="sxs-lookup"><span data-stu-id="07cbc-122">OneNote Developer Reference Copyright Information</span></span>](https://msdn.microsoft.com/library/office/jj680116.aspx)
    
    

