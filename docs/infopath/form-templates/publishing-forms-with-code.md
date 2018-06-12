---
title: Publication de formulaires avec code
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: caafab24-6413-4731-813d-cba3ae9ea97e
description: Un administrateur de collection de sites peut publier des formulaires avec code directement à partir de l’Assistant Publication InfoPath Designer pour une bibliothèque de formulaires sur SharePoint. Le code est exécuté dans un environnement « bac à sable » (sandbox) afin d'éviter que du code malveillant puisse nuire au serveur. On désigne cela par publication d'une solution en bac à sable (sandbox) ou publication sur l'infrastructure sandbox SharePoint.
ms.openlocfilehash: c25243a966bc1dc1a559ccf2ba58fabfadbd94a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782467"
---
# <a name="publishing-forms-with-code"></a><span data-ttu-id="96d12-105">Publication de formulaires avec code</span><span class="sxs-lookup"><span data-stu-id="96d12-105">Publishing Forms with Code</span></span>

<span data-ttu-id="96d12-106">Un administrateur de collection de sites peut publier des formulaires avec code directement à partir de l’Assistant Publication InfoPath Designer pour une bibliothèque de formulaires sur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="96d12-106">Any site collection administrator can publish forms with code directly from the InfoPath Designer publishing wizard to a form library on SharePoint.</span></span> <span data-ttu-id="96d12-107">Le code est exécuté dans un environnement « bac à sable » (sandbox) afin d'éviter que du code malveillant puisse nuire au serveur.</span><span class="sxs-lookup"><span data-stu-id="96d12-107">The code is executed in a sandboxed environment so that malicious code cannot harm the server.</span></span> <span data-ttu-id="96d12-108">On désigne cela par publication d'une solution en bac à sable (sandbox) ou publication sur l'infrastructure sandbox SharePoint.</span><span class="sxs-lookup"><span data-stu-id="96d12-108">This is referred to as publishing a sandboxed solution or publishing to the SharePoint sandbox infrastructure.</span></span>
  
<span data-ttu-id="96d12-109">InfoPath 2010 et SharePoint Server 2010 prennent également en charge les solutions déployées par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="96d12-109">InfoPath 2010 and SharePoint Server 2010 also support administrator-deployed solutions.</span></span> <span data-ttu-id="96d12-110">Un concepteur de formulaires publie des formulaires avec du code dans un magasin local, qui sont ensuite révisés et chargés par un administrateur de batterie SharePoint.</span><span class="sxs-lookup"><span data-stu-id="96d12-110">A form designer publishes forms with code to a local store which are later reviewed and uploaded by a SharePoint farm administrator.</span></span> <span data-ttu-id="96d12-111">La confiance totale est octroyée à ce code, qui peut incorporer des fonctionnalités nécessitant des privilèges élevés tels que E/S fichier.</span><span class="sxs-lookup"><span data-stu-id="96d12-111">The code is given full trust, and can incorporate functionality requiring elevated privileges such as file IO.</span></span>
  
## <a name="comparing-sandboxed-and-administrator-approved-solutions"></a><span data-ttu-id="96d12-112">Comparaison entre les solutions en bac à sable (sandbox) et celles approuvées par l'administrateur</span><span class="sxs-lookup"><span data-stu-id="96d12-112">Comparing Sandboxed and Administrator-approved Solutions</span></span>

<span data-ttu-id="96d12-113">Le tableau suivant récapitule les différences de la publication pour ces deux types de solutions.</span><span class="sxs-lookup"><span data-stu-id="96d12-113">The following table summarizes the differences between publishing sandboxed and administrator-approved solutions.</span></span> 
  
||<span data-ttu-id="96d12-114">**Solutions en bac à sable**</span><span class="sxs-lookup"><span data-stu-id="96d12-114">**Sandboxed Solutions**</span></span>|<span data-ttu-id="96d12-115">**Solutions approuvés par l’administrateur**</span><span class="sxs-lookup"><span data-stu-id="96d12-115">**Administrator-approved Solutions**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="96d12-116">**Autorisations requises**</span><span class="sxs-lookup"><span data-stu-id="96d12-116">**Permissions Required**</span></span> <br/> |<span data-ttu-id="96d12-117">Publiables par tout administrateur de collection de sites.</span><span class="sxs-lookup"><span data-stu-id="96d12-117">Can be published by any site collection administrator.</span></span>  <br/> |<span data-ttu-id="96d12-118">Déployables par un administrateur de batterie.</span><span class="sxs-lookup"><span data-stu-id="96d12-118">Can be deployed by a farm administrator.</span></span>  <br/> |
|<span data-ttu-id="96d12-119">**Publication**</span><span class="sxs-lookup"><span data-stu-id="96d12-119">**Publishing**</span></span> <br/> |<span data-ttu-id="96d12-120">Vous pouvez publier directement à partir d’InfoPath.</span><span class="sxs-lookup"><span data-stu-id="96d12-120">Can be published directly from InfoPath.</span></span>  <br/> |<span data-ttu-id="96d12-121">Déployables en utilisant l’Administration centrale ou l’outil de ligne de commande stsadm.</span><span class="sxs-lookup"><span data-stu-id="96d12-121">Can be deployed using Central Administration or the stsadm command-line tool.</span></span>  <br/> |
|<span data-ttu-id="96d12-122">**Protection**</span><span class="sxs-lookup"><span data-stu-id="96d12-122">**Protection**</span></span> <br/> |<span data-ttu-id="96d12-p104">Le code est exécuté dans un environnement « bac à sable » (sandbox) afin de protéger le serveur contre du code malveillant.</span><span class="sxs-lookup"><span data-stu-id="96d12-p104">Code is run in a sandboxed environment. This helps protect the server from malicious code.</span></span>  <br/> |<span data-ttu-id="96d12-125">Le code peut s’exécuter avec autorisation totale et accéder à toutes les ressources sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="96d12-125">Code can run with full trust and access any resource on the server.</span></span>  <br/> |
|<span data-ttu-id="96d12-126">**Utilisation recommandée**</span><span class="sxs-lookup"><span data-stu-id="96d12-126">**Recommended Use**</span></span> <br/> |<span data-ttu-id="96d12-127">Formulaires nécessitant une petite quantité de code seulement.</span><span class="sxs-lookup"><span data-stu-id="96d12-127">Forms that only require a small amount of code.</span></span>  <br/> |<span data-ttu-id="96d12-128">Formulaires contenant de nombreuses lignes de code.</span><span class="sxs-lookup"><span data-stu-id="96d12-128">Forms that contain many lines of code.</span></span>  <br/> |
   
### <a name="publishing-form-templates-as-sandboxed-solutions"></a><span data-ttu-id="96d12-129">Publication de modèles de formulaire en tant que solutions en bac à sable (sandbox)</span><span class="sxs-lookup"><span data-stu-id="96d12-129">Publishing Form Templates as Sandboxed Solutions</span></span>

<span data-ttu-id="96d12-p105">La publication d'un formulaire avec du code en tant que solution bac à sable n'est pas différente de celle de tout autre formulaire dans une bibliothèque de documents. Utilisez simplement l'assistant de publication comme d'habitude et votre formulaire sera chargé sur le serveur et fonctionnera dans le bac à sable.</span><span class="sxs-lookup"><span data-stu-id="96d12-p105">Publishing a form with code as a sandboxed solution is no different from publishing any other form to a document library. Just use the publishing wizard as usual and your form will be uploaded to the server and will operate in the sandbox.</span></span>
  
<span data-ttu-id="96d12-132">Notez que le déploiement de votre formulaire en tant que solution bac à sable comporte certaines restrictions :</span><span class="sxs-lookup"><span data-stu-id="96d12-132">Note that there are certain restrictions to deploying your form as a sandboxed solution:</span></span>
  
- <span data-ttu-id="96d12-133">Ce doit être un formulaire InfoPath.</span><span class="sxs-lookup"><span data-stu-id="96d12-133">Must be an InfoPath form.</span></span>
    
- <span data-ttu-id="96d12-134">Il doit utiliser C# ou Visual Basic comme langage de programmation.</span><span class="sxs-lookup"><span data-stu-id="96d12-134">Must use C# or Visual Basic as the programming language.</span></span>
    
- <span data-ttu-id="96d12-135">Impossible d’envoyer aux connexions de données de messagerie.</span><span class="sxs-lookup"><span data-stu-id="96d12-135">Cannot submit to email data connections.</span></span>
    
- <span data-ttu-id="96d12-136">Il ne peut pas avoir des propriétés promues pour des connexions partie-à-partie.</span><span class="sxs-lookup"><span data-stu-id="96d12-136">Cannot have properties promoted for part-to-part connections.</span></span>
    
- <span data-ttu-id="96d12-137">Il ne peut pas comporter des connexions de données ni des contrôles de métadonnées gérées.</span><span class="sxs-lookup"><span data-stu-id="96d12-137">Must not have any managed meta-data controls or data connections.</span></span>
    
<span data-ttu-id="96d12-138">Pour permettre aux administrateurs de collection de sites d'utiliser solutions bac à sable sur Microsoft SharePoint Server 2010 ou sur un serveur qui exécute Microsoft SharePoint Foundation 2010, l'administrateur de batterie doit démarrer le service de code utilisateur Windows SharePoint.</span><span class="sxs-lookup"><span data-stu-id="96d12-138">To enable site collection administrators to use sandboxed solutions on Microsoft SharePoint Server 2010 or a server that runs Microsoft SharePoint Foundation 2010, the farm administrator must start the Windows SharePoint User Code service.</span></span>
  
### <a name="to-start-the-windows-sharepoint-user-code-service"></a><span data-ttu-id="96d12-139">Pour démarrer le service de code utilisateur Windows SharePoint</span><span class="sxs-lookup"><span data-stu-id="96d12-139">To start the Windows SharePoint User Code service</span></span>

1. <span data-ttu-id="96d12-140">Ouvrez l'Administration centrale.</span><span class="sxs-lookup"><span data-stu-id="96d12-140">Open Central Administration.</span></span>
    
2. <span data-ttu-id="96d12-141">Sous **Services système**, cliquez sur **Gérer les services sur le serveur**.</span><span class="sxs-lookup"><span data-stu-id="96d12-141">Under **System Services**, click **Manage services on server**.</span></span>
    
3. <span data-ttu-id="96d12-142">Démarrez le **Service de code utilisateur Microsoft SharePoint Foundation**.</span><span class="sxs-lookup"><span data-stu-id="96d12-142">Start the **Microsoft SharePoint Foundation User Code Service**.</span></span>
    
### <a name="to-publish-a-sandboxed-solution"></a><span data-ttu-id="96d12-143">Pour publier une solution en bac à sable (sandbox)</span><span class="sxs-lookup"><span data-stu-id="96d12-143">To publish a sandboxed solution</span></span>

1. <span data-ttu-id="96d12-144">Ouvrez le modèle de formulaire dans le concepteur InfoPath.</span><span class="sxs-lookup"><span data-stu-id="96d12-144">Open the form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="96d12-145">Cliquez sur l'onglet **Fichier**, puis cliquez sur **SharePoint Server** sur l'onglet **Publier** dans Backstage.</span><span class="sxs-lookup"><span data-stu-id="96d12-145">Click the **File** tab, and then click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
    
3. <span data-ttu-id="96d12-146">Entrez l'URL du site SharePoint sur lequel publier, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="96d12-146">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="96d12-147">[!IMPORTANTE] Vous devez être administrateur de collection de sites sur ce site pour publier ce modèle de formulaire en tant que solution bac à sable.</span><span class="sxs-lookup"><span data-stu-id="96d12-147">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
  
4. <span data-ttu-id="96d12-148">Sélectionnez **Bibliothèque de formulaires**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="96d12-148">Select **Form Library**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="96d12-149">Sélectionnez **Créer une bibliothèque de formulaires**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="96d12-149">Select **Create a new form library**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="96d12-150">Entrez le nom et la description de votre bibliothèque de formulaires, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="96d12-150">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
    
7. <span data-ttu-id="96d12-151">Cliquez sur **Publier**.</span><span class="sxs-lookup"><span data-stu-id="96d12-151">Click **Publish**.</span></span>
    
<span data-ttu-id="96d12-152">Pour des exemples de solutions qui illustrent des scénarios appropriés pour la publication de modèles de formulaires en tant que solutions bac à sable, voir [Exemples de solutions en bac à sable (sandbox)](sample-sandboxed-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="96d12-152">For example solutions that demonstrate scenarios that are appropriate for form templates published as sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
### <a name="publishing-form-templates-as-administrator-deployed-solutions"></a><span data-ttu-id="96d12-153">Publication de modèles de formulaires en tant que solutions déployées par un administrateur</span><span class="sxs-lookup"><span data-stu-id="96d12-153">Publishing Form Templates as Administrator-Deployed Solutions</span></span>

<span data-ttu-id="96d12-154">La publication de votre formulaire en tant que modèle approuvé par l'administrateur est recommandée si votre formulaire comporte de nombreuses connexions de données, s'il nécessite la confiance totale, ou si votre modèle doit être défini à l'échelle de la batterie.</span><span class="sxs-lookup"><span data-stu-id="96d12-154">Publishing your form as an administrator-approved template is recommended if your form has many data connections, if it requires full-trust security, or if you require a farm-wide template.</span></span>
  
<span data-ttu-id="96d12-155">Pour un administrateur de batterie, plusieurs étapes sont nécessaires pour fournir une solution déployée par un administrateur sur SharePoint. En tant que développeur, vous devez préparer la solution avant de la soumettre à l'administrateur.</span><span class="sxs-lookup"><span data-stu-id="96d12-155">There are several steps that a farm administrator must complete before an administrator-deployed solution is available on SharePoint, and you as the developer must prepare the solution before the administrator is engaged.</span></span>
  
<span data-ttu-id="96d12-156">Tout d'abord, si votre formulaire doit être déployé avec autorisation totale, vous devez définir le niveau de sécurité comme décrit dans la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="96d12-156">First, if your form is going to be deployed as full trust, you must set the security level as described in the following procedure.</span></span>
  
### <a name="to-set-the-security-level-of-a-form-template-to-full-trust"></a><span data-ttu-id="96d12-157">Pour définir le niveau de sécurité Autorisation totale pour un modèle de formulaire</span><span class="sxs-lookup"><span data-stu-id="96d12-157">To set the security level of a form template to full trust</span></span>

1. <span data-ttu-id="96d12-158">Ouvrez le modèle de formulaire dans le concepteur InfoPath.</span><span class="sxs-lookup"><span data-stu-id="96d12-158">Open the form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="96d12-159">Cliquez sur l'onglet **Fichier**. Sous l'onglet **Informations**, cliquez sur **Options de formulaire**.</span><span class="sxs-lookup"><span data-stu-id="96d12-159">Click the **File** tab, on the **Info** tab click **Form Options**.</span></span>
    
3. <span data-ttu-id="96d12-160">Cliquez sur la catégorie **Sécurité et approbation**, puis désactivez la case à cocher **Déterminer automatiquement le niveau de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="96d12-160">Click the **Security and Trust** category, and then clear the **Automatically determine security level** check box.</span></span> 
    
4. <span data-ttu-id="96d12-161">Sélectionnez **Confiance totale**.</span><span class="sxs-lookup"><span data-stu-id="96d12-161">Select **Full Trust**.</span></span>
    
<span data-ttu-id="96d12-162">Ensuite, publiez le formulaire en suivant la procédure ci-après. Notez qu'elle comporte certaines différences par rapport à la procédure de publication standard.</span><span class="sxs-lookup"><span data-stu-id="96d12-162">Then, publish the form by using the following procedure, but be aware that there are some differences from a standard publishing procedure.</span></span>
  
### <a name="to-publish-an-administrator-deployed-solution"></a><span data-ttu-id="96d12-163">Pour publier une solution déployée par un administrateur</span><span class="sxs-lookup"><span data-stu-id="96d12-163">To publish an administrator-deployed solution</span></span>

1. <span data-ttu-id="96d12-164">Dans la première page de l' **Assistant Publication**, spécifiez l'emplacement du site SharePoint Server 2010 ou SharePoint Foundation 2010, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="96d12-164">In the first page of the **Publishing Wizard**, specify the location of the SharePoint Server 2010 or SharePoint Foundation 2010 site, and then click **Next**.</span></span>
    
2. <span data-ttu-id="96d12-p106">InfoPath active automatiquement la case à cocher **Modèle de formulaire approuvé par l'administrateur** sur la seconde page de l'assistant. Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="96d12-p106">InfoPath will automatically select the **Administrator-approved form template** check box on the second page of the wizard. Click **Next**.</span></span>
    
3. <span data-ttu-id="96d12-p107">La troisième page est destinée uniquement aux scénarios déployés par un administrateur. Au lieu de sélectionner un SharePoint Server, publiez le formulaire dans un magasin local. L'administrateur SharePoint chargera le fichier à partir de cet emplacement durant le processus de déploiement.</span><span class="sxs-lookup"><span data-stu-id="96d12-p107">The third page is unique to administrator-deployed scenarios. Instead of selecting a SharePoint Server, publish the form to a local store. The SharePoint administrator will upload the file from this location during the administrator deployment process.</span></span>
    
4. <span data-ttu-id="96d12-170">Renseignez les pages restantes de l' **Assistant Publication**.</span><span class="sxs-lookup"><span data-stu-id="96d12-170">Complete the remaining pages of the **Publishing Wizard**.</span></span>
    

