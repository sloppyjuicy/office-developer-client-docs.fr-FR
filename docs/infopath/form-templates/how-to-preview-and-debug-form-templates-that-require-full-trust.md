---
title: Aperçu et débogage des modèles de formulaires qui nécessitent une confiance totale
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- debugging [infopath 2007], infopath 2003-compatible form templates,previewing InfoPath 2003-compatible form templates,form templates [InfoPath 2007], previewing 2003-compatible,form templates [InfoPath 2007], debugging 2003-compatible,debugging InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: Par défaut, si vous tentez de déboguer ou d'afficher un projet avec du code managé dont le code appelle un membre de modèle objet qui nécessite une confiance totale, comme la propriété LoginName qui doit accéder aux informations sur le domaine de connexion de l'utilisateur, Microsoft InfoPath affiche les messages d'erreurs suivants.
ms.openlocfilehash: 0780db286e2ca9cef381c2d24cb621c7c243dcb7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411259"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a><span data-ttu-id="89e6e-104">Aperçu et débogage des modèles de formulaires qui nécessitent une confiance totale</span><span class="sxs-lookup"><span data-stu-id="89e6e-104">Preview and Debug Form Templates that Require Full Trust</span></span>

<span data-ttu-id="89e6e-105">Par défaut, si vous tentez de déboguer ou d'afficher un projet avec du code managé dont le code appelle un membre de modèle objet qui nécessite une confiance totale, comme la propriété **LoginName** qui doit accéder aux informations sur le domaine de connexion de l'utilisateur, Microsoft InfoPath affiche les messages d'erreurs suivants.</span><span class="sxs-lookup"><span data-stu-id="89e6e-105">By default, if you attempt to debug or preview a managed-code project that contains code that invokes an object model member that requires full trust, such as the **LoginName** property which requires access to information about the user's login domain, Microsoft InfoPath will display the following error messages.</span></span> 
  
<span data-ttu-id="89e6e-106">En mode Aperçu :</span><span class="sxs-lookup"><span data-stu-id="89e6e-106">When previewing:</span></span>
  
<span data-ttu-id="89e6e-p101">« Une exception non prise en charge s'est produite dans le code du formulaire. », suivi du message d'erreur « InfoPath ne peut pas exécuter cette action en raison d'une erreur dans le code du formulaire."</span><span class="sxs-lookup"><span data-stu-id="89e6e-p101">"An unhandled exception has occurred in the form's code." Followed by, "InfoPath cannot complete this action, because of an error in the form's code."</span></span>
  
<span data-ttu-id="89e6e-109">En mode débogage :</span><span class="sxs-lookup"><span data-stu-id="89e6e-109">When debugging:</span></span>
  
<span data-ttu-id="89e6e-110">L'affichage est ciblé sur la ligne de code dans l'éditeur de code qui appelle le membre requérant une confiance totale, et le message suivant s'affiche : « L'exception **SecurityException** n'a pas été gérée par le code utilisateur - Échec de la demande. »</span><span class="sxs-lookup"><span data-stu-id="89e6e-110">Focus will move to the line of code in the code editor that is calling the member that requires full trust, and the following message will be displayed: " **SecurityException** was unhandled by user code - Request failed".</span></span> 
  
<span data-ttu-id="89e6e-111">Pour permettre à la logique métier d'appeler ce membre lorsqu'il est en cours de débogage ou affiché en mode Aperçu, vous devez définir le niveau de sécurité **Confiance totale** pour votre formulaire, en suivant la procédure décrite ci-après.</span><span class="sxs-lookup"><span data-stu-id="89e6e-111">To allow the form template's business logic to call this member when it is being debugged or previewed, you must set your form template's security level to **Full Trust** as described in the following procedure.</span></span> 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a><span data-ttu-id="89e6e-112">Configuration d'un modèle de formulaire avec code managé qui requiert une confiance totale</span><span class="sxs-lookup"><span data-stu-id="89e6e-112">Configuring a Managed Code Form Template that Requires Full Trust</span></span>

### <a name="set-your-forms-security-level-to-full-trust"></a><span data-ttu-id="89e6e-113">Attribution du niveau de sécurité Confiance totale à un formulaire</span><span class="sxs-lookup"><span data-stu-id="89e6e-113">Set your form's security level to Full Trust</span></span>

1. <span data-ttu-id="89e6e-114">Dans InfoPath, ouvrez le modèle de formulaire en mode Création.</span><span class="sxs-lookup"><span data-stu-id="89e6e-114">In InfoPath, open the form template in design mode.</span></span>
    
2. <span data-ttu-id="89e6e-115">Cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** sous l'onglet **Infos** tab.</span><span class="sxs-lookup"><span data-stu-id="89e6e-115">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="89e6e-116">Dans la liste **Catégorie**, cliquez sur **Sécurité et approbation.**</span><span class="sxs-lookup"><span data-stu-id="89e6e-116">In the **Category** list, click **Security and Trust.**</span></span>
    
4. <span data-ttu-id="89e6e-117">Dans la section **Niveau de sécurité**, désactivez la case à cocher **Déterminer automatiquement le niveau de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="89e6e-117">Under **Security Level**, clear **Automatically determine security level**.</span></span>
    
5. <span data-ttu-id="89e6e-118">Sélectionnez **Confiance totale**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="89e6e-118">Select **Full Trust**, and then click **OK**.</span></span>
    
<span data-ttu-id="89e6e-119">Une fois cette procédure effectuée, vous pouvez déboguer votre projet comme décrit dans l’aperçu et déboguer les modèles de formulaire [InfoPath avec code.](how-to-preview-and-debug-infopath-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="89e6e-119">After this procedure is performed, you can debug your project as described in [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="89e6e-120">[!REMARQUE] Pour réussir le déploiement d'un modèle de formulaire avec code managé qui requiert une confiance totale, vous devez effectuer quelques étapes supplémentaires, notamment la signature numérique, ou l'installation et l'enregistrement du modèle de formulaire.</span><span class="sxs-lookup"><span data-stu-id="89e6e-120">Successfully deploying a managed code form template that requires full trust requires additional steps, such as digitally signing, or installing and registering the form template.</span></span> <span data-ttu-id="89e6e-121">Pour plus d’informations sur le déploiement d’un modèle de formulaire avec code géré après avoir été déboché, voir Déployer des modèles de formulaire [InfoPath avec code.](how-to-deploy-infopath-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="89e6e-121">For information on deploying a managed code form template after it is debugged see, [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="89e6e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89e6e-122">See also</span></span>



[<span data-ttu-id="89e6e-123">Afficher un aperçu et déboguer des modèles de formulaires InfoPath avec code</span><span class="sxs-lookup"><span data-stu-id="89e6e-123">Preview and Debug InfoPath Form Templates with Code</span></span>](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[<span data-ttu-id="89e6e-124">Déployer des modèles de formulaire InfoPath avec code</span><span class="sxs-lookup"><span data-stu-id="89e6e-124">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)

