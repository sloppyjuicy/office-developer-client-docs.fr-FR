---
title: Configuration des paramètres de sécurité pour les modèles de formulaire avec code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- security policy deployment package [infopath 2007],URLs [InfoPath 2007], assigning FullTrust,code access security [InfoPath 2007],UNCs [InfoPath 2007], assigning FullTrust,CAS [InfoPath 2007],security [InfoPath 2007], configuring,code groups [InfoPath 2007],FullTrust [InfoPath 2007], assigning to UNCs,FullTrust [InfoPath 2007], assigning to URLs
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Vous pouvez personnaliser le jeu d'autorisations qui est appliqué à un modèle de formulaire InfoPath avec code managé en utilisant le composant logiciel enfichable Configuration .NET.
ms.openlocfilehash: 77f3546d976bb5ea353aa3fbe58ba7af6cd92a6d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391415"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a><span data-ttu-id="2c0a7-104">Configuration des paramètres de sécurité pour les modèles de formulaire avec code</span><span class="sxs-lookup"><span data-stu-id="2c0a7-104">Configure Security Settings for Form Templates with Code</span></span>

<span data-ttu-id="2c0a7-105">Vous pouvez personnaliser le jeu d'autorisations qui est appliqué à un modèle de formulaire InfoPath avec code managé en utilisant le composant logiciel enfichable Configuration .NET.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-105">You can customize the permission set that is applied to an InfoPath managed code form template by using the .NET Configuration snap-in.</span></span>
  
<span data-ttu-id="2c0a7-p101">Le CLR (Common Language Runtime) utilisé par InfoPath recherche un groupe de codes prédéfini appelé  *Modèles de formulaire InfoPath*  au niveau de la stratégie de l'ordinateur dans le groupe All_Code. Le CLR applique les jeux d'autorisations définis dans ce groupe au domaine d'application (AppDomain) dans lequel le formulaire s'exécute. Ceci vous permet de personnaliser les jeux d'autorisations qui sont accordés aux modèles de formulaire de code managé InfoPath. Par exemple, vous pouvez accorder à un modèle de formulaire téléchargé depuis https://MySite l'autorisation d'accès à Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-p101">The common language runtime (CLR) hosted by InfoPath will look for a predefined code group named  *InfoPath Form Templates*  at the Machine policy level under the All_Code group. The CLR will apply the permission sets that are defined under that group to the application domain (AppDomain) where the form code runs. This enables you to customize the permission sets that are granted to InfoPath managed code form templates. For example, you can grant a form template downloaded from https://MySite permission to access the Active Directory.</span></span> 
  
<span data-ttu-id="2c0a7-110">Pour que la stratégie de sécurité personnalisée définie à l'aide du composant logiciel enfichable Configuration .NET soit appliquée, elle doit être déployée sur tous les ordinateurs clients sur lesquels le modèle de formulaire sera exécuté.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-110">For custom security policy defined by using the .NET Configuration snap-in to be applied, it must be deployed on all the client computers where the form template will run.</span></span>
  
<span data-ttu-id="2c0a7-111">Pour plus d’informations sur le modèle de sécurité pour InfoPath gérée des modèles de formulaires de code, voir [Modèle de sécurité pour les modèles de formulaires avec Code](about-the-security-model-for-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="2c0a7-111">For more information about the security model for InfoPath managed code form templates, see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md)</span></span>
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a><span data-ttu-id="2c0a7-112">Création d'un groupe de codes pour les modèles de formulaire InfoPath</span><span class="sxs-lookup"><span data-stu-id="2c0a7-112">Creating a Code Group for InfoPath Form Templates</span></span>

<span data-ttu-id="2c0a7-p102">La procédure suivante crée un groupe de codes qui n'octroie aucune autorisation aux modèles de formulaire InfoPath avec code managé (à l'exception de ceux qui sont installés ou enregistrés sur votre ordinateur local). Elle vous permet d'attribuer des jeux d'autorisations aux modèles de formulaire InfoPath situés à des URL ou UNC spécifiques. Pour plus d'informations sur la création et l'attribution de jeux d'autorisations à des groupes de codes au sein du groupe de codes  `InfoPath Form Templates`, voir la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-p102">The following procedure will create a code group that grants no permissions to InfoPath managed code form templates (except those that are installed or registered on your local computer) under which you can assign permission sets to InfoPath form templates located at specific URLs or UNCs. For information about how to create and assign permission sets to code groups within the  `InfoPath Form Templates` code group, see the following procedure.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2c0a7-115">[!REMARQUE] Contrairement à l'outil **Configuration Microsoft .NET Framework 1.1** qui est installé avec Microsoft .NET Framework 1.1 Redistributable Package, **Configuration Microsoft .NET Framework 2.0** est uniquement installé avec le Kit de développement logiciel (SDK) Microsoft .NET Framework 2.0.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-115">Unlike the **Microsoft .NET Framework 1.1 Configuration** tool that is installed with the Microsoft .NET Framework 1.1 Redistributable Package, the **Microsoft .NET Framework 2.0 Configuration** is installed only with the Microsoft .NET Framework 2.0 Software Development Kit (SDK).</span></span> 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a><span data-ttu-id="2c0a7-116">Pour créer un groupe de codes de sécurité personnalisé pour les formulaires InfoPath avec code managé</span><span class="sxs-lookup"><span data-stu-id="2c0a7-116">To create a custom security code group for InfoPath managed code forms</span></span>

1. <span data-ttu-id="2c0a7-117">Dans le menu **Démarrer**, pointez sur **Outils d'administration**, puis cliquez sur **Configuration Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-117">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="2c0a7-118">Si l'option **Outils d'administration** ne se trouve pas dans le menu **Démarrer**, ouvrez **Outils d'administration** depuis le **Panneau de configuration** et double-cliquez sur **Configuration Microsoft .NET Framework 2,0**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-118">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="2c0a7-119">Dans **Poste de travail**, développez les nœuds **Stratégie de sécurité du runtime**, **Ordinateur**, **Groupes de codes** et **All_Code**, puis cliquez avec le bouton droit sur le nœud **All_Code** et cliquez sur **Nouveau** pour ouvrir la boîte de dialogue **Créer un groupe de codes**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-119">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then right-click the **All_Code** node and click **New** to open the **Create Code Group** dialog box.</span></span> 
    
3. <span data-ttu-id="2c0a7-120">Attribuez un nom au nouveau groupe de codes  `InfoPath Form Templates` (ce texte doit être exact), puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-120">Name the new code group  `InfoPath Form Templates` (this text must be exact), and then click **Next**.</span></span>
    
4. <span data-ttu-id="2c0a7-121">Définissez le type de condition du groupe de codes sur **Tout le code**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-121">Set the condition type for the code group to **All Code**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="2c0a7-122">Cliquez sur **Utiliser un jeu d'autorisations existant**, affectez le jeu d'autorisations **Nothing** au groupe de codes, cliquez sur **Suivant**, puis sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-122">Click **Use existing permission set**, assign the **Nothing** permission set to the code group, click **Next**, and then click **Finish**.</span></span>
    
6. <span data-ttu-id="2c0a7-123">Pour appliquer les nouveaux paramètres, fermez puis redémarrez InfoPath.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-123">To apply the new settings, close and restart InfoPath.</span></span>
    
<span data-ttu-id="2c0a7-124">Si vous le souhaitez, vous pouvez gérer le jeu d'autorisations pour tous les modèles de formulaire InfoPath avec code managé en attribuant un jeu d'autorisations autre que **Rien** au groupe de codes **Modèles de formulaire InfoPath**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-124">If you prefer, you can manage the permission set for all InfoPath managed code form templates by assigning a permission set other than the **Nothing** permission set to the **InfoPath Form Templates** code group.</span></span> 
> [!NOTE]
> <span data-ttu-id="2c0a7-p103">[!REMARQUE] Vous pouvez modifier à tout moment le jeu d'autorisations d'un groupe de codes de sécurité en cliquant avec le bouton droit sur le groupe dans le composant **Configuration .NET 2,0**, puis en cliquant sur **Propriétés**, puis sur l'onglet **Jeu d'autorisations**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-p103">You can change the permission set for a security code group at any time by right-clicking the group in the . **NET Configuration 2.0** snap-in, clicking **Properties**, and then clicking the **Permission Set** tab.</span></span> 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a><span data-ttu-id="2c0a7-127">Affectation d'une autorisation totale à des formulaires comportant une URL ou une UNC spécifique</span><span class="sxs-lookup"><span data-stu-id="2c0a7-127">Assigning FullTrust to Forms at a Specific URL or UNC</span></span>

<span data-ttu-id="2c0a7-p104">Vous pouvez créer des groupes de codes sous le groupe **Modèles de formulaires InfoPath** pour accorder une autorisation totale à des modèles de formulaires provenant d'une URL ou d'un emplacement UNC spécifique. Ainsi, tous les modèles de formulaires publiés à l'emplacement spécifié s'exécuteront avec une autorisation totale.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-p104">You can create code groups under the **InfoPath Form Templates** group to grant the full trust permission set to form templates from a particular URL or UNC location. After doing this, every form template published to the specified location will run fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2c0a7-130">[!REMARQUE] Un modèle de formulaire chargé depuis l'ordinateur local (groupe de codes de la zone MyComputer) est chargé par InfoPath à l'aide d'une URL aléatoire.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-130">A form template that is loaded from the local computer (My Computer Zone code group) is loaded by InfoPath using a random URL.</span></span> <span data-ttu-id="2c0a7-131">De ce fait, vous ne pouvez pas utiliser la procédure qui suit pour accorder le jeu d'autorisations Autorisation totale à un tel modèle de formulaire.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-131">For this reason, you cannot use the following procedure to grant the FullTrust permission set to such a form template.</span></span> <span data-ttu-id="2c0a7-132">Pour accorder à un modèle de formulaire installé localement l’autorisation FullTrust définie, utilisez une des procédures décrites dans la section « Déploiement de formulaire modèles qui nécessitent totale » de la rubrique [Déploiement des modèles de formulaire InfoPath avec Code](how-to-deploy-infopath-form-templates-with-code.md) .</span><span class="sxs-lookup"><span data-stu-id="2c0a7-132">To grant a locally installed form template the FullTrust permission set, use one of the procedures that are described in the "Deploying Form Templates That Require Full Trust" section of the [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md) topic.</span></span> 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a><span data-ttu-id="2c0a7-133">Pour affecter une autorisation totale aux formulaires InfoPath situés à un emplacement URL ou UNC spécifique</span><span class="sxs-lookup"><span data-stu-id="2c0a7-133">To assign FullTrust to InfoPath forms at a specific URL or UNC location</span></span>

1. <span data-ttu-id="2c0a7-134">Dans le menu **Démarrer**, pointez sur **Outils d'administration**, puis cliquez sur **Configuration Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-134">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="2c0a7-135">Si l'option **Outils d'administration** ne se trouve pas dans le menu **Démarrer**, ouvrez **Outils d'administration** depuis le **Panneau de configuration** et double-cliquez sur **Configuration Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-135">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="2c0a7-136">Dans **Poste de travail**, développez les nœuds **Stratégie de sécurité du runtime**, **Ordinateur**, **Groupes de code**, **All_Code**, puis cliquez sur le nœud **Modèles de formulaires InfoPath**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-136">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then click the **InfoPath Form Templates** node.</span></span> 
    
3. <span data-ttu-id="2c0a7-137">Dans la liste **Tâches** du volet de droite, cliquez sur **Ajouter un groupe de codes enfants**, donnez un nom à ce groupe de codes, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-137">In **Tasks** list in the right pane, click **Add a Child Code Group**, name the code group, and then click **Next**.</span></span>
    
4. <span data-ttu-id="2c0a7-138">Dans la liste **Type de condition pour ce groupe de codes**, sélectionnez **URL**, puis entrez l'URL ou l'UNC de l'emplacement des modèles de formulaires InfoPath avec code managé auxquels vous souhaitez accorder le jeu d'autorisations **Autorisation totale**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-138">In the **Choose the condition type for this code group** list, select **URL**, and then enter the URL or UNC for the location of the InfoPath managed code form templates that you want to grant the **FullTrust** permission set.</span></span> 
    
    <span data-ttu-id="2c0a7-p106">Pour restreindre le jeu d'autorisations à un seul modèle de formulaire, spécifiez le chemin complet de ce modèle de formulaire. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="2c0a7-p106">To restrict the permission set to a single form template, specify the full path of that particular form template. For example:</span></span>
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `https://MySite/MySubsite/MyFormTempate.xsn`
    
    <span data-ttu-id="2c0a7-p107">Pour accorder un jeu d'autorisations à tous les modèles de formulaires d'une URL ou d'une UNC, n'indiquez pas le nom du modèle et ajoutez un astérisque à la fin de l'URL ou de l'UNC. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="2c0a7-p107">To grant the permission set to all form templates in a URL or UNC, omit the name of the template and add an asterisk at the end of the URL or UNC. For example:</span></span>
    
     `\\MyServer\MyShare\*`
    
     `https://MySite/MySubsite/*`
    
5. <span data-ttu-id="2c0a7-143">Cliquez sur **Suivant**, puis sur **Utiliser un jeu d'autorisations existant** et attribuez le jeu d'autorisations **Autorisation totale** au groupe de codes.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-143">Click **Next**, and then click **Use existing permission set** and assign the **FullTrust** permission set to the code group.</span></span> 
    
6. <span data-ttu-id="2c0a7-144">Cliquez sur **Suivant**, puis sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-144">Click **Next**, and then click **Finish**.</span></span>
    
7. <span data-ttu-id="2c0a7-145">Pour appliquer les nouveaux paramètres, fermez puis redémarrez InfoPath.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-145">To apply the new settings, close and restart InfoPath.</span></span>
    
> [!NOTE]
> <span data-ttu-id="2c0a7-146">[!REMARQUE] Pour appliquer un jeu d'autorisations plus restrictif ou personnalisé, sélectionnez l'option appropriée à la place de **Autorisation totale** à l'étape 4.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-146">To apply a more restrictive or custom permission set, select the appropriate option instead of **FullTrust** in step 4.</span></span> 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a><span data-ttu-id="2c0a7-147">Création d'un package de déploiement pour la stratégie de sécurité d'InfoPath</span><span class="sxs-lookup"><span data-stu-id="2c0a7-147">Creating a Deployment Package for InfoPath Security Policy</span></span>

<span data-ttu-id="2c0a7-148">Après avoir défini une stratégie de sécurité personnalisée pour les modèles de formulaires InfoPath avec code managé, vous pouvez créer un package Windows Installer (.msi) pour déployer la stratégie de sécurité sur les ordinateurs des utilisateurs à l'aide de la Stratégie de groupe ou de Microsoft Systems Management Server.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-148">After defining custom security policy for InfoPath managed-form templates, you can create a Windows Installer Package (.msi) to deploy this security policy on users' computers by using Group Policy or Microsoft Systems Management Server.</span></span>
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a><span data-ttu-id="2c0a7-149">Pour créer un package de déploiement pour la stratégie de sécurité personnalisée d'InfoPath</span><span class="sxs-lookup"><span data-stu-id="2c0a7-149">To create a deployment package for custom InfoPath security policy</span></span>

1. <span data-ttu-id="2c0a7-150">Dans le menu **Démarrer**, pointez sur **Outils d'administration**, puis cliquez sur **Configuration Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-150">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="2c0a7-151">Si l'option **Outils d'administration** ne se trouve pas dans le menu **Démarrer**, ouvrez **Outils d'administration** depuis le **Panneau de configuration** et double-cliquez sur **Configuration Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-151">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="2c0a7-152">Cliquez avec le bouton droit sur **Stratégie de sécurité du runtime**, puis cliquez sur **Créer un package de déploiement**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-152">Right-click **Runtime Security Policy**, and then click **Create Deployment Package**.</span></span>
    
3. <span data-ttu-id="2c0a7-153">Sous **Sélectionnez le niveau de stratégie de sécurité à déployer**, cliquez sur **Ordinateur**, spécifiez le dossier et le nom de fichier du package Windows Installer Package, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-153">Under **Select the security policy to deploy**, click **Machine**, specify the folder and file name for the Windows Installer Package, and then click **Next**.</span></span>
    
4. <span data-ttu-id="2c0a7-154">Cliquez sur **Terminer** pour créer le package de déploiement.</span><span class="sxs-lookup"><span data-stu-id="2c0a7-154">Click **Finish** to create the deployment package.</span></span> 
    
5. <span data-ttu-id="2c0a7-155">Pour plus d’informations sur la façon d’utiliser l’outil de Configuration .NET Framework, recherchez aide de Visual Studio ou le site Web MSDN « Outil .NET Framework Configuration (Mscorcfg.msc) ».</span><span class="sxs-lookup"><span data-stu-id="2c0a7-155">For information about how to use the .NET Framework Configuration tool, search Visual Studio Help or the MSDN website for ".NET Framework Configuration Tool (Mscorcfg.msc)".</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c0a7-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c0a7-156">See also</span></span>



[<span data-ttu-id="2c0a7-157">À propos du modèle de sécurité pour les modèles de formulaire avec code</span><span class="sxs-lookup"><span data-stu-id="2c0a7-157">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)

