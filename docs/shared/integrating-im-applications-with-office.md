---
title: Intégration des applications de messagerie instantanée à Office
manager: soliver
ms.date: 07/25/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: Cet article montre comment configurer une application cliente de message instantanée (MI) afin qu'elle intègre des fonctionnalités sociales dans Office 2013, notamment l'affichage de présence et l'envoi de messages instantanés à partir d'une carte de visite.
ms.openlocfilehash: 383aac24be347cf637d9e2f255623035eea8bc40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787945"
---
# <a name="integrating-im-applications-with-office"></a><span data-ttu-id="30a0d-103">Intégration des applications de messagerie instantanée à Office</span><span class="sxs-lookup"><span data-stu-id="30a0d-103">Integrating IM applications with Office</span></span>

<span data-ttu-id="30a0d-104">Cet article montre comment configurer une application cliente de message instantanée (MI) afin qu'elle intègre des fonctionnalités sociales dans Office 2013, notamment l'affichage de présence et l'envoi de messages instantanés à partir d'une carte de visite.</span><span class="sxs-lookup"><span data-stu-id="30a0d-104">This article describes how to configure an instant message (IM) client application so that it integrates with the social features in Office 2013, including displaying presence and sending instant messages from the contact card.</span></span>
  
<span data-ttu-id="30a0d-105">Si vous avez des questions ou commentaires concernant cet article technique ou le processus qu'il décrit, vous pouvez contacter Microsoft directement en envoyant un message électronique à [docthis@microsoft.com](mailto:docthis@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="30a0d-105">If you have any questions or comments about this technical article or the processes that it describes, you can contact Microsoft directly by sending an email to [docthis@microsoft.com](mailto:docthis@microsoft.com).</span></span>
  
## <a name="introduction"></a><span data-ttu-id="30a0d-106">Introduction</span><span class="sxs-lookup"><span data-stu-id="30a0d-106">Introduction</span></span>
<span data-ttu-id="30a0d-107"><a name="off15_IMIntegration_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-107"></span></span>

<span data-ttu-id="30a0d-p101">Office 2013 permet une intégration enrichie avec les applications clientes de messagerie instantanée, y compris Lync 2013. Cette intégration fournit aux utilisateurs des fonctionnalités de messagerie instantanée à partir de Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013 et OneNote 2013 ainsi qu'une intégration de présence sur les pages SharePoint 2013. Les utilisateurs peuvent voir la photo, le nom, le statut de présence et les données de contact des personnes de leur liste de contacts. Ils peuvent démarrer une session de messagerie instantanée, passer un appel vidéo ou appeler directement à partir de la carte de visite (l'élément d'interface utilisateur dans Office 2013 affichant les options de communication et les informations de contact). Office 2013 vous permet de rester facilement connecté à vos contacts sans vous forcer à quitter votre messagerie électronique ou vos documents.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p101">Office 2013 provides rich integration with IM client applications, including Lync 2013. This integration provides users with IM capabilities from within Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013, and OneNote 2013 as well as providing presence integration on SharePoint 2013 pages. Users can see the photo, name, presence status, and contact data for people in their contacts list. They can start an IM session, video call, or phone call directly from the contact card (the UI element in Office 2013 that surfaces contact information and communication options). Office 2013 makes it easy to stay connected to your contacts without taking you outside of your email or documents.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="30a0d-p102">Cet article utilise le terme application cliente de messagerie instantanée pour faire spécifiquement référence à l'application installée sur l'ordinateur d'un utilisateur qui communique vers le service de messagerie instantanée. Par exemple, Lync 2013 est considérée comme une application cliente de messagerie instantanée. Cet article ne fournit pas de détails sur la façon dont l'application cliente de messagerie instantanée communique avec le service de messagerie instantanée ou sur le service de messagerie instantanée lui-même.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p102">This article uses the term IM client application to refer specifically to the application installed on a user's computer that communicates to the IM service. For example, Lync 2013 is considered an IM client application. This article does not provide details about how the IM client application communicates to the IM service or about the IM service itself.</span></span> 
  
<span data-ttu-id="30a0d-p103">Vous pouvez personnaliser une application cliente de messagerie instantanée afin qu’elle communique avec Office. Vous pouvez notamment modifier votre application de messagerie instantanée pour qu’elle affiche les informations suivantes dans l’interface utilisateur d’Office :</span><span class="sxs-lookup"><span data-stu-id="30a0d-p103">You can customize an IM client application so that it communicates with Office. Specifically, you can modify your IM application so that it displays the following information within the Office UI:</span></span>
  
- <span data-ttu-id="30a0d-118">Photo du contact</span><span class="sxs-lookup"><span data-stu-id="30a0d-118">Contact photo.</span></span>
    
- <span data-ttu-id="30a0d-119">Nom du contact</span><span class="sxs-lookup"><span data-stu-id="30a0d-119">Contact name.</span></span>
    
- <span data-ttu-id="30a0d-120">Note de statut personnel du contact</span><span class="sxs-lookup"><span data-stu-id="30a0d-120">Contact personal status note.</span></span>
    
- <span data-ttu-id="30a0d-121">Statut de la présence du contact</span><span class="sxs-lookup"><span data-stu-id="30a0d-121">Contact presence status.</span></span>
    
- <span data-ttu-id="30a0d-122">Chaîne de disponibilité du contact (par exemple, « Disponible » ou « Absent(e) du bureau »)</span><span class="sxs-lookup"><span data-stu-id="30a0d-122">Contact availability string (for example, "Available" or "Out of Office").</span></span>
    
- <span data-ttu-id="30a0d-123">Chaîne de niveau d’aptitude du contact (par exemple, « Prêt pour la vidéo »)</span><span class="sxs-lookup"><span data-stu-id="30a0d-123">Contact capability string (for example, "Video Ready").</span></span>
    
- <span data-ttu-id="30a0d-124">Lancement de messagerie instantanée en un clic</span><span class="sxs-lookup"><span data-stu-id="30a0d-124">One-click IM launch.</span></span>
    
- <span data-ttu-id="30a0d-125">Lancement d’un appel vidéo en un clic</span><span class="sxs-lookup"><span data-stu-id="30a0d-125">One-click video call launch.</span></span>
    
- <span data-ttu-id="30a0d-126">Lancement d’appel téléphonique en un clic (avec les fonctionnalités SIP, numéro de téléphone, messagerie vocale et appel de nouveau numéro).</span><span class="sxs-lookup"><span data-stu-id="30a0d-126">One-click phone call launch (including SIP, phone number, voice mail, and call new number).</span></span>
    
- <span data-ttu-id="30a0d-127">Gestion du contact (ajouter au groupe de messagerie instantanée)</span><span class="sxs-lookup"><span data-stu-id="30a0d-127">Contact management (add to IM group).</span></span>
    
- <span data-ttu-id="30a0d-128">Emplacement et fuseau horaire du contact</span><span class="sxs-lookup"><span data-stu-id="30a0d-128">Contact location and time zone.</span></span>
    
- <span data-ttu-id="30a0d-129">Données du contact, numéro de téléphone, adresse de messagerie, poste et nom de sa société</span><span class="sxs-lookup"><span data-stu-id="30a0d-129">Contact data, phone number, email address, title, and company name.</span></span>
    
<span data-ttu-id="30a0d-130">**Figure 1. Carte de visite dans Office 2013**</span><span class="sxs-lookup"><span data-stu-id="30a0d-130">**Figure 1. Contact card in Office 2013**</span></span>

<span data-ttu-id="30a0d-131">![La carte de visite dans Office 2013](media/ocom15_peoplecard.png "La carte de visite dans Office 2013")</span><span class="sxs-lookup"><span data-stu-id="30a0d-131">![The People Card in Office 2013](media/ocom15_peoplecard.png "The People Card in Office 2013")</span></span>
  
<span data-ttu-id="30a0d-p104">Pour permettre cette intégration dans Office, l'application cliente de messagerie instantanée doit implémenter un ensemble d'interfaces fournies par Office pour établir une connexion. Les API nécessaires à cette intégration sont incluses dans l'espace de noms [UCCollborationLib](http://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) figurant dans le fichier Microsoft.Office.UC.dll installé avec les versions de Office 2013, comprenant Lync et Skype Entreprise. L'espace de noms **UCCollaborationLib** inclut les interfaces que vous devez implémenter pour intégrer Office.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p104">To enable this integration with Office, an IM client application must implement a set of interfaces that Office provides to connect to it. The APIs for this integration are included in the [UCCollborationLib](http://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) namespace that is contained in the Microsoft.Office.UC.dll file, which is installed with versions of Office 2013 that include Lync / Skype for Business. The **UCCollaborationLib** namespace includes the interfaces that you must implement to integrate with Office.</span></span> 
  
> [!IMPORTANT] 
> <span data-ttu-id="30a0d-135">La bibliothèque de types pour les interfaces requises est incorporée à Lync 2013/Skype Entreprise.</span><span class="sxs-lookup"><span data-stu-id="30a0d-135">Important: The type library for the required interfaces is embedded in Lync 2013/Skype for Business.</span></span> <span data-ttu-id="30a0d-136">Pour les intégrateurs tiers, cela fonctionne uniquement lorsque Lync 2013 et Skype Entreprise sont installés sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="30a0d-136">For third-party integrators, this works only when both Lync 2013 and Skype for Business are installed on the target machine.</span></span> <span data-ttu-id="30a0d-137">Si vous intégrez à l'aide d'Office Standard, vous devez extraire la bibliothèque de types et l'installer sur l'ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="30a0d-137">If you are integrating using Office Standard, you need to extract the type library and install it on the target machine.</span></span> <span data-ttu-id="30a0d-138">Le [kit de développement logiciel (SDK) Lync 2013](https://www.microsoft.com/en-us/download/details.aspx?id=36824) inclut le fichier Microsoft.Office.UC.dll.</span><span class="sxs-lookup"><span data-stu-id="30a0d-138">The [Lync 2013 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=36824) includes the Microsoft.Office.UC.dll file.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="30a0d-139">Une multitude d'applications Office 2010 peuvent également s'intégrer à une application de fournisseur de messagerie instantanée tierce : Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010 et SharePoint Server 2010 (à l'aide d'un contrôle ActiveX).</span><span class="sxs-lookup"><span data-stu-id="30a0d-139">A handful of Office 2010 applications can integrate similarly with a third-party IM provider application: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010, and SharePoint Server 2010 (using an ActiveX control).</span></span> <span data-ttu-id="30a0d-140">Nombre des étapes nécessaires pour l’intégration avec Office 2013 s’appliquent aussi à Office 2010.</span><span class="sxs-lookup"><span data-stu-id="30a0d-140">Many of the steps required for integration with Office 2013 apply to Office 2010 as well.</span></span> <span data-ttu-id="30a0d-141">Il existe plusieurs différences dans la manière dont Office 2010 est intégré avec une application de fournisseur de messagerie instantanée :</span><span class="sxs-lookup"><span data-stu-id="30a0d-141">There are several key differences in how off14short integrates with an IM provider application:</span></span> 
>  - <span data-ttu-id="30a0d-142">Office 2010 n’affiche pas la photo du contact.</span><span class="sxs-lookup"><span data-stu-id="30a0d-142">off14short does not display the contact's photo.</span></span> 
>  - <span data-ttu-id="30a0d-143">Vous devez télécharger le fichier Microsoft.Office.Uc.dll indépendamment d’Office 2010.</span><span class="sxs-lookup"><span data-stu-id="30a0d-143">>  You must download the Microsoft.Office.Uc.dll file separately from Office 2010.</span></span> <span data-ttu-id="30a0d-144">Le [SDK Lync 2010](http://www.microsoft.com/en-us/download/details.aspx?id=18898) inclut le fichier Microsoft.Office.UC.dll pour Office 2010.</span><span class="sxs-lookup"><span data-stu-id="30a0d-144">The [Lync 2010 SDK](http://www.microsoft.com/en-us/download/details.aspx?id=18898) includes the Microsoft.Office.UC.dll file for Office 2010.</span></span> 
>  - <span data-ttu-id="30a0d-145">Lorsque l’application Office appelle la méthode [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) dans l’application cliente de messagerie instantanée, elle transfère la chaîne « 14.0.0.0 ».</span><span class="sxs-lookup"><span data-stu-id="30a0d-145">When the Office application calls the [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) method on the IM client application, it passes in the string "14.0.0.0".</span></span> 
>  - <span data-ttu-id="30a0d-146">Office 2010 énumère tous les groupes et les contacts dès qu'il se connecte à une application cliente de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-146">>  Office 2010 enumerates all groups and contacts as soon as it connects to an IM client application.</span></span> 
  
## <a name="how-office-integrates-with-an-im-client-application"></a><span data-ttu-id="30a0d-147">Intégration d’Office à une application cliente de messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="30a0d-147">How Office integrates with an IM client application</span></span>
<span data-ttu-id="30a0d-148"><a name="off15_IMIntegration_How"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-148"></span></span>

<span data-ttu-id="30a0d-149">Quand une application Office 2013 démarre, elle suit le processus suivant pour s'intégrer à l'application cliente de messagerie instantanée par défaut :</span><span class="sxs-lookup"><span data-stu-id="30a0d-149">When an Office 2013 application starts, it goes through the following process to integrate with the default IM client application:</span></span>
  
1. <span data-ttu-id="30a0d-150">Elle vérifie le Registre pour identifier l’application cliente de messagerie instantanée par défaut et se connecte ensuite à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="30a0d-150">It checks the registry to discover the default IM client application and then connects to it.</span></span>
    
2. <span data-ttu-id="30a0d-151">Elle s’authentifie avec l’application cliente de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-151">It authenticates with the IM client application.</span></span>
    
3. <span data-ttu-id="30a0d-152">Elle se connecte à des interfaces spécifiques qui sont exposées par l’application cliente de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-152">It connects to specific interfaces that are exposed by the IM client application.</span></span>
    
4. <span data-ttu-id="30a0d-153">Elle détermine les fonctionnalités de l’utilisateur connecté (utilisateur local), notamment l’obtention des contacts de l’utilisateur, détermine la présence de l’utilisateur et ses fonctionnalités de messagerie instantanée (messagerie instantanée, conversation vidéo, appels VoIP etc.).</span><span class="sxs-lookup"><span data-stu-id="30a0d-153">It determines the capabilities of the currently signed-in user (local user), including getting the user's contacts, determining the user's presence, and determining the user's IM capabilities (instant messaging, video chat, VOIP, and so on).</span></span>
    
5. <span data-ttu-id="30a0d-154">Elle obtient les informations de présence des contacts de l’utilisateur local.</span><span class="sxs-lookup"><span data-stu-id="30a0d-154">It gets presence information for the local user's contacts.</span></span>
    
6. <span data-ttu-id="30a0d-155">Lorsque l'application cliente de messagerie instantanée s'arrête, l'application Office 2013 se déconnecte sans assistance.</span><span class="sxs-lookup"><span data-stu-id="30a0d-155">When the IM client application shuts down, the Office 2013 application silently disconnects.</span></span>
    
### <a name="discovering-the-im-application"></a><span data-ttu-id="30a0d-156">Détection de l’application de messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="30a0d-156">Discovering the IM application</span></span>

<span data-ttu-id="30a0d-p108">L’application Office recherche plusieurs clés et entrées spécifiques dans le Registre pour détecter l’application cliente de messagerie instantanée par défaut. Si elle détecte une application cliente de messagerie instantanée par défaut, elle tente de s’y connecter.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p108">The Office application looks for several specific keys and entries in the registry to discover the default IM client application. If it discovers a default IM client application, it then attempts to connect to it.</span></span>
  
<span data-ttu-id="30a0d-159">L’application Office suit le processus suivant pour découvrir l’application cliente de messagerie instantanée par défaut :</span><span class="sxs-lookup"><span data-stu-id="30a0d-159">The process that the Office application goes through to discover the default IM client application is as follows:</span></span>
  
1. <span data-ttu-id="30a0d-160">L’application Office vérifie si la sous-clé HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp du Registre est définie et lit le nom de l’application mentionnée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-160">The Office application looks to see if the HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp subkey in the registry is set and reads the application name listed there.</span></span>
    
2. <span data-ttu-id="30a0d-161">Ensuite, l'application Office lit la clé HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning et suit les modifications de sa valeur.</span><span class="sxs-lookup"><span data-stu-id="30a0d-161">The Office application then reads the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key and monitors the value for changes.</span></span>
    
3. <span data-ttu-id="30a0d-162">Puis elle lit la clé de Registre HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_ et obtient les valeurs du ProcessName et de l'ID de classe (CLSID) stockées à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="30a0d-162">The Office application next reads the HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_ registry key and gets the ProcessName and class ID (CLSID) values stored there.</span></span> 
    
4. <span data-ttu-id="30a0d-163">Lorsque l'application cliente de messagerie instantanée a réussi sa séquence de démarrage et a enregistré toutes les classes correctement pour l'intégration de présence, elle définit la clé HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning sur « 2 », ce qui indique que l'application cliente est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="30a0d-163">Once the IM client application has completed its start sequence successfully and registered all of the classes correctly for the presence integration, it sets the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key to "2", indicating that the client application is running.</span></span>
    
5. <span data-ttu-id="30a0d-164">Lorsque l'application Office détecte que la clé HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning a la valeur « 2 », elle recherche le nom du processus de l'application cliente de messagerie instantanée dans la liste des processus en cours d'exécution sur l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="30a0d-164">When the Office application discovers that the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key has been set to "2", it checks the list of running processes on the computer for the process name of the IM client application.</span></span>
    
6. <span data-ttu-id="30a0d-165">Lorsque l'application Office trouve le processus qui utilise l'application cliente de messagerie instantanée, elle appelle **CoCreateInstance** à l'aide du CLSID pour établir une connexion à l'application cliente de messagerie instantanée sous la forme d'un serveur COM hors processus.</span><span class="sxs-lookup"><span data-stu-id="30a0d-165">Once the Office application finds the process that the IM client application uses, the Office application calls **CoCreateInstance** using the CLSID to establish a connection to the IM client application as an out-of-process COM server.</span></span> 
    
### <a name="authenticating-the-connection-to-the-im-application"></a><span data-ttu-id="30a0d-166">Authentification de la connexion à l’application de messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="30a0d-166">Authenticating the connection to the IM application</span></span>

<span data-ttu-id="30a0d-167">Lorsque l’application Office établit une connexion à l’application cliente de messagerie instantanée, elle effectue ensuite les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="30a0d-167">After the Office application establishes a connection to the IM client application, it then does the following:</span></span>
  
1. <span data-ttu-id="30a0d-168">Elle appelle la méthode [IUnknown::QueryInterface](http://msdn.microsoft.com/fr-FR/library/ms682521%28v=VS.85%29.aspx) pour vérifier l'interface [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration).</span><span class="sxs-lookup"><span data-stu-id="30a0d-168">The Office application calls [IUnknown::QueryInterface](http://msdn.microsoft.com/fr-FR/library/ms682521%28v=VS.85%29.aspx) method to check for the [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) interface.</span></span> 
    
2. <span data-ttu-id="30a0d-169">Puis elle appelle la méthode **IUCOfficeIntegration.GetAuthenticationInfo**, en transmettant la version d'intégration prise en charge la plus récente (par exemple, « 15.0.0.0 »).</span><span class="sxs-lookup"><span data-stu-id="30a0d-169">The Office application then calls the **IUCOfficeIntegration.GetAuthenticationInfo** method, passing in the highest supported integration version (for example, "15.0.0.0").</span></span> 
    
3. <span data-ttu-id="30a0d-170">Si l’application cliente de messagerie instantanée prend en charge la version d’Office transmise en tant que paramètre, l’application renvoie la chaîne XML codée en dur suivante vers le code appelant :</span><span class="sxs-lookup"><span data-stu-id="30a0d-170">If the IM client application supports the version of Office passed in as a parameter, the application returns the following hard-coded XML string to the calling code:</span></span>
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > <span data-ttu-id="30a0d-171">Pour des raisons d'héritage, si l'application cliente de messagerie instantanée prend en charge la version d'Office transmise en tant que paramètre, elle doit renvoyer la valeur  `<authenticationinfo>` exacte vers l'appel à destination de **GetAuthenticationInfo**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-171">For legacy reasons, the IM client application must return the exact value  `<authenticationinfo>` to the call to **GetAuthenticationInfo** if it supports the version of Office passed in as a parameter.</span></span> 
  
4. <span data-ttu-id="30a0d-172">Si l'application cliente de messagerie instantanée ne parvient pas à renvoyer une valeur, l'application Office appelle la méthode **GetAuthenticationInfo** à l'aide de la version d'Office prise en charge précédant la version la plus récente (par exemple, « 14.0.0.0 »).</span><span class="sxs-lookup"><span data-stu-id="30a0d-172">If the IM client application fails to return a value, the Office application calls the **GetAuthenticationInfo** method again with the next highest supported version of Office (for example, "14.0.0.0").</span></span> 
    
5. <span data-ttu-id="30a0d-p109">Lorsqu'Office détermine que l'application cliente de messagerie instantanée prend en charge l'intégration de la messagerie instantanée et de la présence, il se connecte à un ensemble d'interfaces pour terminer l'initialisation. Pour plus d'informations, voir [Connexion aux interfaces requises](#off15_IMIntegration_HowConnect).</span><span class="sxs-lookup"><span data-stu-id="30a0d-p109">Once Office determines that the IM client application supports IM and presence integration, it connects to a required set of interfaces to finish initializing. (For more information, see [Connecting to required interfaces](#off15_IMIntegration_HowConnect).)</span></span>
    
<span data-ttu-id="30a0d-175">Si l’application Office rencontre une erreur lors d’une des étapes précédentes, elle reprend le processus et l’intégration de la présence n’est pas rétablie pendant la session de l’application Office.</span><span class="sxs-lookup"><span data-stu-id="30a0d-175">If the Office application encounters an error on any of the steps above, it backs out and presence integration is not established again during the session of the Office application.</span></span> 
  
### <a name="connecting-to-required-interfaces"></a><span data-ttu-id="30a0d-176">Connexion aux interfaces requises</span><span class="sxs-lookup"><span data-stu-id="30a0d-176">Connecting to required interfaces</span></span>
<span data-ttu-id="30a0d-177"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-177"></span></span>

<span data-ttu-id="30a0d-p110">Après avoir authentifié la connexion à l’application cliente de messagerie instantanée, l’application Office essaie de se connecter à un ensemble d’interfaces requises que l’application cliente de messagerie instantanée doit exposer. L’application Office effectue cela en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="30a0d-p110">After authenticating the connection to the IM client application, the Office application attempts to connect to a set of required interfaces that the IM client application must expose. The Office application accomplishes this by doing the following:</span></span>
  
- <span data-ttu-id="30a0d-180">L'application Office obtient un objet [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) en appelant la méthode **IUCOfficeIntegration.GetInterface**, en transférant la constante **oiInterfaceLyncClient** à partir de l'énumération [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface).</span><span class="sxs-lookup"><span data-stu-id="30a0d-180">The Office application gets an [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceLyncClient** constant from the [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> 
    
- <span data-ttu-id="30a0d-181">L'application Office obtient un objet [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) en appelant la méthode **IUCOfficeIntegration.GetInterface**, en transmettant la constante **oiInterfaceAutomation** à partir de l'énumération **OIInterface**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-181">The Office application gets an [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceAutomation** constant from the **OIInterface** enumeration.</span></span> 
    
- <span data-ttu-id="30a0d-182">L'application Office configure le détecteur d'événements [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient).</span><span class="sxs-lookup"><span data-stu-id="30a0d-182">The Office application sets up the [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) event listener.</span></span> 
    
- <span data-ttu-id="30a0d-183">L'application Office configure le détecteur d'événements [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration).</span><span class="sxs-lookup"><span data-stu-id="30a0d-183">The Office application sets up the [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) event listener.</span></span> 
    
- <span data-ttu-id="30a0d-184">L'application Office obtient l'état de connexion à partir de l'application cliente de messagerie instantanée en accédant à la propriété **ILyncClient.State**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-184">The Office application gets the sign-in state from the IM client application by accessing the **ILyncClient.State** property.</span></span> 
    
- <span data-ttu-id="30a0d-185">L'application Office obtient les fonctionnalités de l'application cliente de messagerie instantanée en appelant la méthode **IUCOfficeIntegration.GetSupportedFeatures**, qui renvoie un indicateur de l'énumération [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature).</span><span class="sxs-lookup"><span data-stu-id="30a0d-185">The Office application gets the capabilities of the IM client application by calling the **IUCOfficeIntegration.GetSupportedFeatures** method, which returns a flag from the [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> 
    
- <span data-ttu-id="30a0d-186">L'application Office accède à la propriété **ILyncClient.Self** pour obtenir une référence à un objet [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf).</span><span class="sxs-lookup"><span data-stu-id="30a0d-186">The Office application accesses the **ILyncClient.Self** property to get a reference to an [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) object.</span></span> 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a><span data-ttu-id="30a0d-187">Récupération des fonctionnalités de l’utilisateur local</span><span class="sxs-lookup"><span data-stu-id="30a0d-187">Retrieving the capabilities of the local user</span></span>
<span data-ttu-id="30a0d-188"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-188"></span></span>

<span data-ttu-id="30a0d-189">L’application Office procède comme suit pour obtenir les fonctionnalités de l’utilisateur local :</span><span class="sxs-lookup"><span data-stu-id="30a0d-189">The Office application gets the capabilities of the local user by doing the following:</span></span>
  
1. <span data-ttu-id="30a0d-190">Si l'application cliente de messagerie instantanée prend en charge l'interface **IClient2**, Office tente d'obtenir un objet [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) en accédant à la propriété **IClient2.PrivateContactManager**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-190">If the IM client application supports the **IClient2** interface, Office tries to get an [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) object by accessing the **IClient2.PrivateContactManager** property.</span></span> 
    
2. <span data-ttu-id="30a0d-p111">Si l'application de messagerie instantanée ne prend pas en charge l'interface **IClient2**, l'application Office obtient un objet **IContactManager** en accédant à la propriété **ILyncClient.ContactManager**. L'application cliente de messagerie instantanée doit renvoyer un objet **IContactManager** avant de pouvoir établir d'autres fonctionnalités de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p111">If the IM application does not support the **IClient2** interface, Office application gets an **IContactManager** object by accessing the **ILyncClient.ContactManager** property. The IM client application must successfully return an **IContactManager** object before any other IM capabilities can be established.</span></span> 
    
3. <span data-ttu-id="30a0d-193">L'application Office accède à la propriété **ILyncClient.Uri**, puis appelle **IContactManager.GetContactByUri** pour obtenir l'objet [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) associé à l'utilisateur local.</span><span class="sxs-lookup"><span data-stu-id="30a0d-193">The Office application accesses the **ILyncClient.Uri** property and then calls **IContactManager.GetContactByUri** to get the [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) object associated with the local user.</span></span> 
    
4. <span data-ttu-id="30a0d-194">L'application effectue plusieurs appels vers **IContact.CanStart** pour établir les fonctionnalités de l'utilisateur local, en transmettant successivement les valeurs de **ModalityTypes.ucModalityInstantMessage** et **ModalityTypes.ucModalityAudioVideo**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-194">The Office application then makes several calls to **IContact.CanStart** to establish the capabilities of the local user, passing in the values for **ModalityTypes.ucModalityInstantMessage** and **ModalityTypes.ucModalityAudioVideo** successively.</span></span> 
    
### <a name="retrieving-contact-presence"></a><span data-ttu-id="30a0d-195">Récupération de la présence du contact</span><span class="sxs-lookup"><span data-stu-id="30a0d-195">Retrieving contact presence</span></span>
<span data-ttu-id="30a0d-196"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-196"></span></span>

<span data-ttu-id="30a0d-197">L’application Office procède comme suit pour obtenir la présence du contact, notamment de l’utilisateur local :</span><span class="sxs-lookup"><span data-stu-id="30a0d-197">The Office application gets contact presence, including the local user, by doing the following:</span></span> 
  
1. <span data-ttu-id="30a0d-198">L'application Office appelle **IContact.GetContactInformation** pour obtenir un élément de la présence du contact.</span><span class="sxs-lookup"><span data-stu-id="30a0d-198">The Office application calls **IContact.GetContactInformation** to get a presence item from the contact.</span></span> 
    
2. <span data-ttu-id="30a0d-p112">Puis elle s'abonne aux modifications de statut de présence du contact. Elle appelle **IContactManager.CreateSubscription** pour obtenir un objet [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription). Elle appelle ensuite **IContactSubscription.AddContact** pour ajouter le contact à l'abonnement, puis appelle **IContactSubscription.Subscribe** pour obtenir les modifications de statut du contact.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p112">The Office application then subscribes to presence status changes from the contact. It calls **IContactManager.CreateSubscription** to get an [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) object. It then calls **IContactSubscription.AddContact** to add the contact to the subscription and then calls **IContactSubscription.Subscribe** to get changes in the contact's status.</span></span> 
    
3. <span data-ttu-id="30a0d-202">Si l'application de messagerie instantanée prend en charge **IContact2**, Office tente d'obtenir les informations de présence en appelant **IContact2.BatchGetContactInformation2**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-202">If the IM application supports **IContact2**, Office attempts to get presence information by calling **IContact2.BatchGetContactInformation2**.</span></span>
    
4. <span data-ttu-id="30a0d-p113">Puis elle récupère les propriétés de présence du contact en appelant **IContact.BatchGetContactInformation**. L'application Office peut obtenir un second jeu de propriétés de présence en accédant à la propriété **IContact.Settings**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p113">The Office application then retrieves the presence properties for the contact by calling **IContact.BatchGetContactInformation**. The Office application can get a second set of presence properties by accessing the **IContact.Settings** property.</span></span> 
    
5. <span data-ttu-id="30a0d-p114">Enfin, l'application Office obtient l'appartenance de groupe du contact en accédant à la propriété **IContact.CustomGroups**. Ceci renvoie une collection [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) qui contient tous les objets [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) auxquels appartient le contact.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p114">Finally, the Office application gets the contact's group membership by accessing the **IContact.CustomGroups** property. This returns an [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) collection that includes all of the [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) objects that the contact belongs to.</span></span> 
    
### <a name="disconnecting-from-the-im-application"></a><span data-ttu-id="30a0d-207">Déconnexion de l’application de messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="30a0d-207">Disconnecting from the IM application</span></span>
<span data-ttu-id="30a0d-208"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-208"></span></span>

<span data-ttu-id="30a0d-p115">Lorsque l'application Office 2013 détecte l'événement **OnShuttingDown** à partir de l'application de messagerie instantanée, elle se déconnecte sans assistance. Toutefois, si l'application Office s'arrête avant l'application de messagerie instantanée, l'application Office n'assure pas le nettoyage de la connexion. L'application de messagerie instantanée doit gérer les fuites de connexion du client.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p115">When the Office 2013 application detects the **OnShuttingDown** event from the IM application, it disconnects silently. However, if the Office application shuts down before the IM application, the Office application does not guarantee that the connection is cleaned up. The IM application must handle client connection leaks.</span></span> 
  
## <a name="setting-registry-keys-and-entries"></a><span data-ttu-id="30a0d-212">Configuration des clés et des entrées de Registre</span><span class="sxs-lookup"><span data-stu-id="30a0d-212">Setting registry keys and entries</span></span>
<span data-ttu-id="30a0d-213"><a name="off15_IMIntegration_SetRegistry"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-213"></span></span>

<span data-ttu-id="30a0d-p116">Comme indiqué précédemment, les applications Office 2013 compatibles avec la messagerie instantanée recherchent des clés, des entrées et des valeurs spécifiques dans le Registre pour découvrir l'application cliente de messagerie instantanée à laquelle se connecter. Ces valeurs de Registre fournissent à l'application Office le nom du processus et le GUID de la classe qui sert de point d'entrée au modèle d'objet de l'application cliente de messagerie instantanée (autrement dit, la classe qui implémente l'interface **IUCOfficeIntegration**). L'application Office co-crée cette catégorie et se connecte en tant que client au serveur COM hors processus dans l'application cliente de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p116">As mentioned previously, the IM-capable Office 2013 applications look for specific keys, entries, and values in the registry to discover the IM client application to connect to. These registry values provide the Office application with the process name and CLSID of the class that acts as the entry point to the IM client application's object model (that is, the class that implements the **IUCOfficeIntegration** interface). The Office application co-creates that class and connects as a client to the out-of-process COM server in the IM client application.</span></span> 
  
<span data-ttu-id="30a0d-217">Utilisez le tableau 1 pour identifier les clés, les entrées et les valeurs qui doivent être écrites dans le Registre pour intégrer une application cliente de messagerie instantanée à Office.</span><span class="sxs-lookup"><span data-stu-id="30a0d-217">Use Table 1 to identify the keys, entries, and values that must be written in the registry to integrate an IM client application with Office.</span></span>
  
<span data-ttu-id="30a0d-218">**Tableau 1. Clés de Registre pour la configuration de l'application cliente de messagerie instantanée par défaut**</span><span class="sxs-lookup"><span data-stu-id="30a0d-218">**Table 1. Registry keys for setting the default IM client application**</span></span>

|<span data-ttu-id="30a0d-219">**Clé**</span><span class="sxs-lookup"><span data-stu-id="30a0d-219">**Key**</span></span>|<span data-ttu-id="30a0d-220">**Entrée**</span><span class="sxs-lookup"><span data-stu-id="30a0d-220">**Entry**</span></span>|<span data-ttu-id="30a0d-221">**Type**</span><span class="sxs-lookup"><span data-stu-id="30a0d-221">**Type**</span></span>|<span data-ttu-id="30a0d-222">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="30a0d-222">**Value**</span></span>|<span data-ttu-id="30a0d-223">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="30a0d-223">**Example**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="30a0d-224">HKEY_LOCAL_MACHINE\Software\IM Internet\\<Nom de l'application\></span><span class="sxs-lookup"><span data-stu-id="30a0d-224">HKEY_LOCAL_MACHINE\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="30a0d-225">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="30a0d-225">FriendlyName</span></span>  <br/> |<span data-ttu-id="30a0d-226">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="30a0d-226">REG_SZ</span></span>  <br/> |<span data-ttu-id="30a0d-227">Nom de l’application cliente de messagerie instantanée tierce.</span><span class="sxs-lookup"><span data-stu-id="30a0d-227">The name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="30a0d-228">Litware IM 2012</span><span class="sxs-lookup"><span data-stu-id="30a0d-228">Litware IM 2012</span></span>  <br/> |
||<span data-ttu-id="30a0d-229">ProcessName</span><span class="sxs-lookup"><span data-stu-id="30a0d-229">ProcessName</span></span>  <br/> |<span data-ttu-id="30a0d-230">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="30a0d-230">REG_SZ</span></span>  <br/> |<span data-ttu-id="30a0d-231">Nom du processus de l’application cliente de messagerie instantanée tierce.</span><span class="sxs-lookup"><span data-stu-id="30a0d-231">The process name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="30a0d-232">litware.exe</span><span class="sxs-lookup"><span data-stu-id="30a0d-232">litware.exe</span></span>  <br/> |
||<span data-ttu-id="30a0d-233">GUID</span><span class="sxs-lookup"><span data-stu-id="30a0d-233">GUID</span></span>  <br/> |<span data-ttu-id="30a0d-234">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="30a0d-234">REG_SZ</span></span>  <br/> |<span data-ttu-id="30a0d-235">ID de classe (CLSID) pour la classe racine pouvant être co-créée dans l'application de messagerie instantanée (il s'agit de la classe qui implémente l'interface **IUCOfficeIntegration**).</span><span class="sxs-lookup"><span data-stu-id="30a0d-235">A class ID (CLSID) for the root, cocreatable class in the IM application (the class that implements the **IUCOfficeIntegration** interface).</span></span>  <br/> |<span data-ttu-id="30a0d-236">Un GUID</span><span class="sxs-lookup"><span data-stu-id="30a0d-236">(A GUID)</span></span>  <br/> |
|<span data-ttu-id="30a0d-237">HKEY_CURRENT_USER\Software\IM Providers</span><span class="sxs-lookup"><span data-stu-id="30a0d-237">HKEY_CURRENT_USER\Software\IM Providers</span></span>  <br/> |<span data-ttu-id="30a0d-238">DefaultIMApp</span><span class="sxs-lookup"><span data-stu-id="30a0d-238">DefaultIMApp</span></span>  <br/> |<span data-ttu-id="30a0d-239">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="30a0d-239">REG_SZ</span></span>  <br/> |<span data-ttu-id="30a0d-p117">Nom de l’application cliente de messagerie instantanée. Il doit s’agir du même nom que celui de la clé de Registre de niveau supérieur (ruche) HKEY_LOCAL_MACHINE.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p117">The name of the IM client application. This must be the same as the name at the top-level registry key (hive) in the HKEY_LOCAL_MACHINE.</span></span>  <br/> |<span data-ttu-id="30a0d-242">Litware</span><span class="sxs-lookup"><span data-stu-id="30a0d-242">Litware</span></span>  <br/> |
|<span data-ttu-id="30a0d-243">HKEY_CURRENT_USER\Software\IM Providers\\<Nom de l'application\></span><span class="sxs-lookup"><span data-stu-id="30a0d-243">HKEY_CURRENT_USER\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="30a0d-244">UpAndRunning</span><span class="sxs-lookup"><span data-stu-id="30a0d-244">UpAndRunning</span></span>  <br/> |<span data-ttu-id="30a0d-245">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="30a0d-245">REG_DWORD</span></span>  <br/> | <span data-ttu-id="30a0d-246">Nombre entier compris entre 0 et 2.</span><span class="sxs-lookup"><span data-stu-id="30a0d-246">An integer value between 0 and 2:</span></span>  <br/>  <span data-ttu-id="30a0d-247">0 : n’est pas en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="30a0d-247">0—Not running</span></span>  <br/>  <span data-ttu-id="30a0d-248">1 : en cours de démarrage</span><span class="sxs-lookup"><span data-stu-id="30a0d-248">1—Starting</span></span>  <br/>  <span data-ttu-id="30a0d-249">2 : en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="30a0d-249">2—Running</span></span>  <br/> <br/><span data-ttu-id="30a0d-250">**Remarque**: la clé de Registre du nom de l’application doit être identique à la valeur de l’entrée DefaultIMApp.</span><span class="sxs-lookup"><span data-stu-id="30a0d-250">The application name registry key must be the same as the value of the DefaultIMApp entry.</span></span>           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a><span data-ttu-id="30a0d-251">Implémentation des interfaces requises pour l’intégration avec Office</span><span class="sxs-lookup"><span data-stu-id="30a0d-251">Implementing the required interfaces for integration with Office</span></span>
<span data-ttu-id="30a0d-252"><a name="off15_IMIntegration_ImplementRequired"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-252"></span></span>

<span data-ttu-id="30a0d-p118">Le fichier exécutable (ou le serveur COM) d'une application cliente de messagerie instantanée doit implémenter trois interfaces à partir de l'espace de noms **UCCollaborationLib** pour pouvoir s'intégrer à Office. Dans le cas contraire, l'application Office reprend le processus durant l'initialisation et la connexion avec l'application cliente de messagerie instantanée n'est pas établie.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p118">There are three interfaces from the **UCCollaborationLib** namespace that the executable (or COM server) of an IM client application must implement so that it can integrate with Office. If these interfaces are not implemented, the Office application backs out during the initialization process and the connection with the IM client application is not established.</span></span> 
  
<span data-ttu-id="30a0d-255">Les interfaces suivantes sont requises :</span><span class="sxs-lookup"><span data-stu-id="30a0d-255">The required interfaces are as follows:</span></span>
  
- <span data-ttu-id="30a0d-256">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) : même si elle n'est pas obligatoire, l'interface **_IUCOfficeIntegrationEvents** doit également être implémentée dans la même classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-256">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)—Although not required, the **_IUCOfficeIntegrationEvents** interface should also be implemented in the same derived class.</span></span> 
    
- <span data-ttu-id="30a0d-257">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) : même si elle n'est pas obligatoire, l'interface **_ILyncClientEvents** doit également être implémentée dans la même classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-257">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)—Although not required, the **_ILyncClientEvents** interface should also be implemented in the same derived class.</span></span> 
    
- [<span data-ttu-id="30a0d-258">IAutomation</span><span class="sxs-lookup"><span data-stu-id="30a0d-258">IAutomation</span></span>](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a><span data-ttu-id="30a0d-259">Interface IUCOfficeIntegration</span><span class="sxs-lookup"><span data-stu-id="30a0d-259">IUCOfficeIntegration interface</span></span>
<span data-ttu-id="30a0d-260"><a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-260"></span></span>

<span data-ttu-id="30a0d-p119">L'interface **IUCOfficeIntegration** fournit le point d'entrée permettant à une application Office de se connecter à l'application cliente de messagerie instantanée. L'interface définit trois méthodes qu'une application Office appelle dans le cadre du processus d'initialisation d'une connexion avec l'application cliente de messagerie instantanée. La classe qui implémente l'interface **IUCOfficeIntegration** doit pouvoir être co-créée pour qu'Office puisse co-créer une instance de celle-ci. En outre, elle doit exposer le CLSID entré en tant que valeur de l'entrée GUID dans la clé de Registre HKEY_LOCAL_MACHINE\Software\IM Providers\  _Application name_.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p119">The **IUCOfficeIntegration** interface provides the entry-point for an Office application to connect to the IM client application. The interface defines three methods that an Office application calls as part of the process of initiating a connection with the IM client application. The class that implements the **IUCOfficeIntegration** interface must be co-creatable so that Office can co-create an instance of it. In addition, it must expose the CLSID that is entered as the value for the GUID entry in the HKEY_LOCAL_MACHINE\Software\IM Providers\  _Application name_ registry key.</span></span> 
  
<span data-ttu-id="30a0d-p120">La classe qui hérite de **IUCOfficeIntegration** doit également implémenter l'interface **_IUCOfficeIntegrationEvents**. L'interface **_IUCOfficeIntegrationEvents** contient les membres qui exposent les gestionnaires d'événements de l'interface **IUCOfficeIntegration**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p120">The class that inherits from **IUCOfficeIntegration** should also implement the **_IUCOfficeIntegrationEvents** interface. The **_IUCOfficeIntegrationEvents** interface contains the members that expose the event handlers of the **IUCOfficeIntegration** interface.</span></span> 
  
<span data-ttu-id="30a0d-267">Le tableau 2 indique les membres qui doivent implémentés dans la classe qui hérite de **IUCOfficeIntegration** et **_IUCOfficeIntegration**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-267">Table 2 shows the members that must be implemented in the class that inherits from **IUCOfficeIntegration** and **_IUCOfficeIntegration**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="30a0d-268">Pour plus d'informations sur les interfaces **IUCOfficeIntegration** et **_IUCOfficeIntegrationEvents**, ainsi que sur leurs membres, consultez [UCCollaborationLib.IUCOfficeIntegration](http://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) et [UCCollaborationLib._IUCOfficeIntegrationEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span><span class="sxs-lookup"><span data-stu-id="30a0d-268">For more information about the **IUCOfficeIntegration** and **_IUCOfficeIntegrationEvents** interfaces and their members, see [UCCollaborationLib.IUCOfficeIntegration](http://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) and [UCCollaborationLib._IUCOfficeIntegrationEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span></span> 
  
<span data-ttu-id="30a0d-269">**Tableau 2. Implémentation des interfaces IUCOfficeIntegration et _IUCOfficeIntegrationEvents**</span><span class="sxs-lookup"><span data-stu-id="30a0d-269">**Table 2. Implementation of the IUCOfficeIntegration and _IUCOfficeIntegrationEvents interfaces**</span></span>

|<span data-ttu-id="30a0d-270">**Interface**</span><span class="sxs-lookup"><span data-stu-id="30a0d-270">**Interface**</span></span>|<span data-ttu-id="30a0d-271">**Membre**</span><span class="sxs-lookup"><span data-stu-id="30a0d-271">**Member**</span></span>|<span data-ttu-id="30a0d-272">**Description**</span><span class="sxs-lookup"><span data-stu-id="30a0d-272">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30a0d-273">**IUCOfficeIntegration**</span><span class="sxs-lookup"><span data-stu-id="30a0d-273">**IUCOfficeIntegration**</span></span> <br/> |<span data-ttu-id="30a0d-274">Méthode **GetAuthenticationInfo**</span><span class="sxs-lookup"><span data-stu-id="30a0d-274">**GetAuthenticationInfo** method</span></span>  <br/> |<span data-ttu-id="30a0d-275">Obtient la chaîne d’informations d’authentification.</span><span class="sxs-lookup"><span data-stu-id="30a0d-275">Gets the authentication info string.</span></span>  <br/> |
||<span data-ttu-id="30a0d-276">Méthode **GetInterface**</span><span class="sxs-lookup"><span data-stu-id="30a0d-276">**GetInterface** method</span></span>  <br/> |<span data-ttu-id="30a0d-277">Obtient l’interface d’une version spécifique.</span><span class="sxs-lookup"><span data-stu-id="30a0d-277">Gets the interface of a particular version.</span></span>  <br/> |
||<span data-ttu-id="30a0d-278">Méthode **GetSupportedFeatures**</span><span class="sxs-lookup"><span data-stu-id="30a0d-278">**GetSupportedFeatures** method</span></span>  <br/> |<span data-ttu-id="30a0d-279">Obtient les fonctionnalités d’intégration Office prises en charge.</span><span class="sxs-lookup"><span data-stu-id="30a0d-279">Gets the supported Office integration features.</span></span>  <br/> |
|<span data-ttu-id="30a0d-280">**_IUCOfficeIntegrationEvents**</span><span class="sxs-lookup"><span data-stu-id="30a0d-280">**_IUCOfficeIntegrationEvents**</span></span> <br/> |<span data-ttu-id="30a0d-281">Événement **OnShuttingDown**</span><span class="sxs-lookup"><span data-stu-id="30a0d-281">**OnShuttingDown** event</span></span>  <br/> |<span data-ttu-id="30a0d-282">Événement déclenché lorsque l’application cliente de messagerie instantanée est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-282">The event raised when the IM client application is trying to shut down.</span></span>  <br/> |
   
<span data-ttu-id="30a0d-283">Utilisez le code suivant pour définir une classe qui hérite des interfaces **IUCOfficeIntegration** et **_IUCOfficeIntegration** au sein d'une application cliente de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-283">Use the following code to define a class that inherits from the **IUCOfficeIntegration** and **_IUCOfficeIntegration** interfaces within an IM client application.</span></span> 
  
```cs
// An example of a class that can be co-created and can integrate
// with Office as an IM provider.
[ClassInterface(ClassInterfaceType.None)]
[ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
[Guid("{CLSID value}"), ComVisible(true)]
public class LitwareClientAppObject : IUCOfficeIntegration
{
    // Implementation details omitted.
}

```

<span data-ttu-id="30a0d-284">La méthode **GetAuthenticationInfo** prend une chaîne comme argument pour le paramètre  _version_.</span><span class="sxs-lookup"><span data-stu-id="30a0d-284">The **GetAuthenticationInfo** method takes a string as an argument for the  _version_ parameter.</span></span> <span data-ttu-id="30a0d-285">Lorsque l’application Office appelle cette méthode, elle transfert l’une des deux chaînes comme argument, en fonction de la version d’Office.</span><span class="sxs-lookup"><span data-stu-id="30a0d-285">When the Office application calls this method, it passes in one of two strings for the argument, depending on the version of Office.</span></span> <span data-ttu-id="30a0d-286">Lorsque l'application Office fournit la méthode avec la version d'Office prise en charge par l'application cliente de messagerie instantanée (autrement dit, qui prend en charge la fonctionnalité), la méthode **GetAuthenticationInfo** renvoie une chaîne XML `<authenticationinfo>` codée en dur.</span><span class="sxs-lookup"><span data-stu-id="30a0d-286">When the Office application supplies the method with the version of Office that the IM client application supports (that is, supports the functionality), the **GetAuthenticationInfo** method returns a hard-coded XML string "`<authenticationinfo>`".</span></span> 
  
<span data-ttu-id="30a0d-287">Utilisez le code suivant pour implémenter la méthode **GetAuthentication** dans le code d’application cliente de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-287">Use the following code to implement the **GetAuthentication** method within the IM client application code.</span></span> 
  
```cs
public string GetAuthenticationInfo(string _version)
{
    // Define the version of Office that the IM client application supports.
    string supportedOfficeVersion = "15.0.0.0";
    // Do a simple check for equivalency.
    if (supportedOfficeVersion == _version)
    {
        // If the version of Office is supported, this method must 
        // return the string literal "<authenticationinfo>" exactly.
        return "<authenticationinfo>";
    }
    else
    {
        return null;
    }
}

```

<span data-ttu-id="30a0d-p122">La méthode **GetInterface** transmet les références aux classes vers le code appelant, en fonction de l'argument transmis pour le paramètre  _interface_. Lorsqu'une application Office appelle la méthode **GetInterface**, elle transfert une des deux valeurs pour le paramètre de l'interface : soit la constante **oiInterfaceILyncClient** (1) ou la constante **oiInterfaceIAutomation** (2) de l'énumération [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface). Si l'application Office transfère la constante **oiInterfaceILyncClient**, la méthode **GetInterface** renvoie une référence à une classe qui implémente l'interface **ILyncClient**. Si l'application Office transfère la constante **oiInterfaceIAutomation**, la méthode **GetInterface** renvoie une classe qui implémente l'interface **IAutomation**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p122">The **GetInterface** method shuttles references to classes to the calling code, depending on what is passed in as an argument for the  _interface_ parameter. When an Office application calls the **GetInterface** method, it passes in one of two values for the interface parameter: either the **oiInterfaceILyncClient** constant (1) or the **oiInterfaceIAutomation** constant (2) of the [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration. If the Office application passes in the **oiInterfaceILyncClient** constant, the **GetInterface** method returns a reference to a class that implements the **ILyncClient** interface. If the Office application passes in the **oiInterfaceIAutomation** constant, the **GetInterface** method returns a class that implements the **IAutomation** interface.</span></span> 
  
<span data-ttu-id="30a0d-292">Utilisez le code suivant pour implémenter la méthode **GetInterface** dans le code de l'application cliente de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-292">Use the following code example to implement the **GetInterface** method within the IM client application code.</span></span> 
  
```cs
public object GetInterface(string _version, OIInterface _interface)
{
    // These objects implement the ILyncClient or IAutomation 
    // interfaces respectively. There is no restriction on what these
    // classes are named.
    IMClient imClient = new IMClient();
    IMClientAutomation imAutomation = new IMClientAutomation();
    // Return different object references depending on the value passed in
    // for the _interface parameter.
    switch (_interface)
    {
        // The calling code is asking for an object that inherits
        // from ILyncClient, so it returns such an object.
        case OIInterface.oiInterfaceILyncClient:
        {
            return imClient;
        }
        // The calling code is asking for an object that inherits
        // from IAutomation, so it returns such an object.
        case OIInterface.oiInterfaceIAutomation:
        {
            return imAutomation;
        }
        default:
        {
            throw new NotImplementedException();
        }
    }
}

```

<span data-ttu-id="30a0d-p123">La méthode **GetSupportedFeatures** renvoie des informations sur les fonctionnalités de messagerie instantanée prises en charge par l'application cliente de messagerie instantanée. Elle prend une chaîne uniquement pour son paramètre,  _version_. Lorsque l'application Office appelle la méthode **GetSupportFeatures**, celle-ci renvoie une valeur à partir de l'énumération [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature). La valeur renvoyée définit les fonctionnalités du client de messagerie instantanée, où chaque fonctionnalité de l'application cliente de messagerie instantanée est indiquée à l'application Office par l'ajout d'un indicateur à la valeur.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p123">The **GetSupportedFeatures** method returns information about the IM features that the IM client application supports. It takes a string for its only parameter,  _version_. When the Office application calls the **GetSupportFeatures** method, the method returns a value from the [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration. The returned value specifies the capabilities of the IM client, where each capability of the IM client application is indicated to the Office application by adding a flag to the value.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="30a0d-297">Les applications Office 2013 ignorent les constantes suivantes dans l’énumération **OIFeature** :</span><span class="sxs-lookup"><span data-stu-id="30a0d-297">Office 2013 applications ignore the following constants in the **OIFeature** enumeration: > oiFeaturePictures (2) > oiFeatureFreeBusyIntegrationoiFeaturePhoneNormalization</span></span> 
> - <span data-ttu-id="30a0d-298">**oiFeaturePictures** (2)</span><span class="sxs-lookup"><span data-stu-id="30a0d-298">**oiFeaturePictures** (2)</span></span> 
> - <span data-ttu-id="30a0d-299">**oiFeatureFreeBusyIntegration**</span><span class="sxs-lookup"><span data-stu-id="30a0d-299">**oiFeatureFreeBusyIntegration**</span></span>
> - <span data-ttu-id="30a0d-300">**oiFeaturePhoneNormalization**</span><span class="sxs-lookup"><span data-stu-id="30a0d-300">**oiFeaturePhoneNormalization**</span></span>
  
<span data-ttu-id="30a0d-301">Utilisez le code suivant pour implémenter la méthode **GetSupportFeatures** dans le code de l’application cliente de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-301">Use the following code example to implement the **GetSupportFeatures** method within the IM client application code.</span></span> 
  
```cs
public OIFeature GetSupportedFeatures(string _version)
{
    OIFeature supportedFeature1 = OIFeature.oiFeatureQuickContacts;
    OIFeature supportedFeature2 = OIFeature.oiFeatureFastSearch;
    return (supportedFeature1 | supportedFeature2);
}

```

### <a name="ilyncclient-interface"></a><span data-ttu-id="30a0d-302">Interface ILyncClient</span><span class="sxs-lookup"><span data-stu-id="30a0d-302">ILyncClient interface</span></span>
<span data-ttu-id="30a0d-303"><a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-303"></span></span>

<span data-ttu-id="30a0d-p124">L'interface **ILyncClient** mappe vers les fonctionnalités de l'application cliente de messagerie instantanée. Elle expose les propriétés qui font référence à la personne connectée à l'application (l'utilisateur local, représenté par l'interface [UCCollaborationLib.ISelf](http://msdn.microsoft.com/library/UCCollaborationLib.ISelf)), l'état de l'application, la liste des contacts de l'utilisateur local, ainsi que d'autres paramètres. Lorsqu'elle tente de se connecter à l'application cliente de messagerie instantanée, l'application Office obtient une référence à un objet qui implémente l'interface **ILyncClient**. À partir de cette référence, Office peut accéder à la plupart des fonctionnalités de l'application cliente de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p124">The **ILyncClient** interface maps to the capabilities of the IM client application itself. It exposes properties that refer to the person who is signed into the application (the local user, represented by the [UCCollaborationLib.ISelf](http://msdn.microsoft.com/library/UCCollaborationLib.ISelf) interface), the state of the application, the list of contacts for the local user, and several other settings. When it's trying to connect to the IM client application, the Office application gets a reference to an object that implements the **ILyncClient** interface. From that reference, Office can access much of the functionality of the IM client application.</span></span> 
  
<span data-ttu-id="30a0d-p125">En outre, la classe qui implémente l'interface **ILyncClient** doit également implémenter l'interface **_ILyncClientEvents**. L'interface **_ILyncClientEvents** expose plusieurs événements requis pour surveiller l'état de l'application cliente de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p125">In addition, the class that implements the **ILyncClient** interface should also implement the **_ILyncClientEvents** interface. The **_ILyncClientEvents** interface exposes several of the events that are required for monitoring the state of the IM client application.</span></span> 
  
<span data-ttu-id="30a0d-310">Le tableau 3 affiche les membres qui doivent être implémentés dans la classe qui hérite de **ILyncClient** et **_ILyncClientEvents**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-310">Table 3 shows the members that must be implemented in the class that inherits from **ILyncClient** and **_ILyncClientEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="30a0d-311">Tout membre de l'interface **ILyncClient** ou **\_ILyncClientEvents** non répertorié dans le tableau doit être présent, mais ne doit pas nécessairement être implémenté.</span><span class="sxs-lookup"><span data-stu-id="30a0d-311">Any member of the ILyncClient or _ILyncClientEvents interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="30a0d-312">Les membres présents, mais non implémentés, peuvent générer une erreur **NotImplementedException** ou **E\_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-312">Members that are present but not implemented can throw a NotImplementedException or E_NOTIMPL error.</span></span> 
> 
> <span data-ttu-id="30a0d-313">Pour plus d'informations sur les interfaces **ILyncClient** et **_ILyncClientEvents**, ainsi que leurs membres, consultez [UCCollaborationLib.ILyncClient](http://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) et [UCCollaborationLib._ILyncClientEvents](http://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span><span class="sxs-lookup"><span data-stu-id="30a0d-313">> For more information about the **ILyncClient** and **_ILyncClientEvents** interfaces and their members, see [UCCollaborationLib.ILyncClient](http://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) and [UCCollaborationLib._ILyncClientEvents](http://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span></span> 
  
<span data-ttu-id="30a0d-314">**Tableau 3. Implémentation des interfaces ILyncClient et ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="30a0d-314">**Table 3. Implementation of ILyncClient and ILyncClientEvents interfaces**</span></span>

|<span data-ttu-id="30a0d-315">**Interface**</span><span class="sxs-lookup"><span data-stu-id="30a0d-315">**Interface**</span></span>|<span data-ttu-id="30a0d-316">**Membre**</span><span class="sxs-lookup"><span data-stu-id="30a0d-316">**Member**</span></span>|<span data-ttu-id="30a0d-317">**Description**</span><span class="sxs-lookup"><span data-stu-id="30a0d-317">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30a0d-318">**ILyncClient**</span><span class="sxs-lookup"><span data-stu-id="30a0d-318">**ILyncClient**</span></span> <br/> |<span data-ttu-id="30a0d-319">Propriété **ContactManager**</span><span class="sxs-lookup"><span data-stu-id="30a0d-319">**ContactManager** property</span></span>  <br/> |<span data-ttu-id="30a0d-320">Obtient le Gestionnaire de groupe de contacts.</span><span class="sxs-lookup"><span data-stu-id="30a0d-320">Gets the contact group manager.</span></span>  <br/> |
||<span data-ttu-id="30a0d-321">Propriété **ConversationManager**</span><span class="sxs-lookup"><span data-stu-id="30a0d-321">**ConversationManager** property</span></span>  <br/> |<span data-ttu-id="30a0d-322">Obtient le Gestionnaire de conversations.</span><span class="sxs-lookup"><span data-stu-id="30a0d-322">Gets the conversations manager.</span></span>  <br/> |
||<span data-ttu-id="30a0d-323">Propriété **Self**</span><span class="sxs-lookup"><span data-stu-id="30a0d-323">**Self** property</span></span>  <br/> |<span data-ttu-id="30a0d-324">Obtient l'objet **Self**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-324">Gets the **Self** object.</span></span>  <br/> |
||<span data-ttu-id="30a0d-325">Méthode **SignIn**</span><span class="sxs-lookup"><span data-stu-id="30a0d-325">**SignIn** method</span></span>  <br/> |<span data-ttu-id="30a0d-326">Démarre le processus de connexion de l’application cliente de messagerie instantanée avec une disponibilité spécifique.</span><span class="sxs-lookup"><span data-stu-id="30a0d-326">Starts the IM client application sign-in process with a specific availability.</span></span>  <br/> |
||<span data-ttu-id="30a0d-327">Propriété **State**</span><span class="sxs-lookup"><span data-stu-id="30a0d-327">**State** property</span></span>  <br/> |<span data-ttu-id="30a0d-328">Obtient l’état actuel de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="30a0d-328">Gets the current platform state.</span></span>  <br/> |
||<span data-ttu-id="30a0d-329">Propriété **Uri**</span><span class="sxs-lookup"><span data-stu-id="30a0d-329">**Uri** property</span></span>  <br/> |<span data-ttu-id="30a0d-330">Obtient l’URI de l’application cliente de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-330">Gets the URI of the IM client application.</span></span>  <br/> |
|<span data-ttu-id="30a0d-331">**_ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="30a0d-331">**_ILyncClientEvents**</span></span> <br/> |<span data-ttu-id="30a0d-332">Événement **OnStateChanged**</span><span class="sxs-lookup"><span data-stu-id="30a0d-332">**OnStateChanged** event</span></span>  <br/> |<span data-ttu-id="30a0d-p127">Déclenché lorsque l'état de l'application cliente de messagerie instantanée est modifié. Vous devez gérer cet événement et obtenir la propriété **eventData.NewState**. L'événement est déclenché pour tous les processus liés à l'instance d'une application cliente de messagerie instantanée lorsqu'un sous-système de l'application entraîne la modification de l'état.  </span><span class="sxs-lookup"><span data-stu-id="30a0d-p127">Raised when the IM client application state changes. You should handle this event and get the **eventData.NewState** property. The event is raised for all processes bound to an instance of an IM client application when any subsystem in the application causes the state change.  </span></span><br/> |
   
<span data-ttu-id="30a0d-p128">Pendant le processus d'initialisation, Office accède à la propriété **ILyncClient.State**. Cette propriété doit renvoyer une valeur à partir de l'énumération [UCCollaborationLib.ClientState](http://msdn.microsoft.com/library/UCCollaborationLib.ClientState).</span><span class="sxs-lookup"><span data-stu-id="30a0d-p128">During the initialization process, Office accesses the **ILyncClient.State** property. This property needs to return a value from the [UCCollaborationLib.ClientState](http://msdn.microsoft.com/library/UCCollaborationLib.ClientState) enumeration.</span></span> 
  
```cs
private ClientState _clientState;
public ClientState State
{
    get
    {
        return this._clientState;
    }
}

```

<span data-ttu-id="30a0d-p129">La propriété **State** stocke l'état actuel de l'application cliente de messagerie instantanée. Elle doit être définie et mise à jour dans l'ensemble de la session d'application cliente de messagerie instantanée. Lorsque l'application cliente de messagerie instantanée se connecte, se déconnecte ou s'arrête, elle doit définir la propriété **State**. Il est préférable de définir cette propriété dans les méthodes **ILyncClient.SignIn** et **ILyncClient.SignOut**, comme l'indique l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p129">The **State** property stores the current status of the IM client application. It must be set and updated throughout the IM client application session. When the IM client application signs in, signs out, or shuts down, it should set the **State** property. It is best to set this property within the **ILyncClient.SignIn** and **ILyncClient.SignOut** methods, as the following example demonstrates.</span></span> 
  
```cs
// This field is of a type that implements the 
// IAsynchronousOperation interface.
private IMClientAsyncOperation _asyncOperation = new IMClientAsyncOperation();
// This field is of a type that implements the ISelf interface.
private IMClientSelf _self;
public IMClientAsyncOperation SignIn(string _userUri, string _domainAndUser, 
    string _password, object _IMClientCallback, object _state)
{
    ClientState _previousClientState = this._clientState;
    this._clientState = ClientState.ucClientStateSignedIn;
    // The IMClientStateChangedEventData class implements the 
    // IClientStateChangedEventData interface.
    IMClientStateChangedEventData eventData = 
        new IMClientStateChangedEventData(_previousClientState, 
        this._clientState);
    if (_userUri != null)
    {
        // During the sign-in process, create a new contact with
        // the contact information of the currently signed-in user.
        this._self = new IMClientSelf(IMContact.BuildContact(_userUri));
    }
    // Raise the _ILyncClientEvents.OnStateChanged event.
    OnStateChanged(this, eventData as UC.ClientStateChangedEventData);
    
    return this._asyncOperation;
    }
}

```

<span data-ttu-id="30a0d-342">L'exemple de code suivant montre comment configurer le détecteur d'événements à l'aide des interfaces _ **ILyncClientEvents** et _ **IUCOfficeIntegrationEvents**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-342">The following code example demonstrates how to set up the event listener using the _ **ILyncClientEvents** and _ **IUCOfficeIntegrationEvents** interfaces.</span></span> 
  
```cs
using Microsoft.Office.Uc;
using System;
using System.Runtime.CompilerServices;
using System.Runtime.InteropServices;
namespace SampleImplementation
{
    // Note: UCOfficeIntegration inherits from both IUCOfficeIntegration and _IUCOfficeIntegrationEvents_Event
    [ClassInterface(ClassInterfaceType.None), Guid("13c41ef9-eb90-4e94-8a7c-1e9d686bc019"), ComVisible(true)]
    [ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
    public class MyInstantMessengerOfficeIntegration : UCOfficeIntegration
    {
        #region IUCOfficeIntegration implementation
        public string GetAuthenticationInfo(string _version)
        {
            return "";
        }
        public object GetInterface(string _version, OIInterface _interface)
        {
            return null;
        }
        public OIFeature GetSupportedFeatures(string _version)
        {
            return OIFeature.oiFeatureAddOneNoteToConversation;
        }
        #endregion
        #region _IUCOfficeIntegrationEvents support
        // This event implements void _IUCOfficeIntegrationEvents.OnShuttingDown();
        public event _IUCOfficeIntegrationEvents_OnShuttingDownEventHandler OnShuttingDown;
        // This method is called by the IM application when it is beginning to shut down.
        // The method will raise the OnShuttingDown event which is translated by .NET COM interop layer
        // into a call to _IUCOfficeIntegrationEvents.OnShuttingDown.
        // This notifies Office applications that the IM application is going away.
        internal void RaiseOnShuttingDownEvent()
        {
            if (this.OnShuttingDown != null)
            {
                this.OnShuttingDown();
            }
        }
        #endregion
    }
    // Note: LyncClient inherits from both ILyncClient and _ILyncClientEvents_Event
    // You must implement LyncClient because the event handlers in _ILyncClientEvents expect you to pass a LyncClient interface.
    [ComVisible(true)]
    [ComSourceInterfaces(typeof(_ILyncClientEvents))]
    public class MyInstantMessengerOfficeIntegration2 :
        Client,
        Client2,
        LyncClient
    {
        #region Interfaces
        public LyncClientCapabilityTypes Capabilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConferenceScheduler ConferenceScheduler
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager ContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConversationManager ConversationManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DelegatorClient[] DelegatorClients
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DeviceManager DeviceManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public bool InSuppressedMode
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager PrivateContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public RoomManager RoomManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Self Self
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientSettings Settings
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public SignInConfiguration SignInConfiguration
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientState State
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientType Type
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public string Uri
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Utilities Utilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ApplicationRegistration CreateApplicationRegistration(string _appGuid, string _appName)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Initialize(string _clientName, string _version = "0", string _clientShortName = "0", string _clientNameAbbreviation = "0", string _clientLongName = "0", SupportedFeatures _supportedFeatures = SupportedFeatures.ucAllFeatures, [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Shutdown([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignIn(string _userUri = "0", string _domainAndUsername = "0", string _password = "0", [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignOut([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        #endregion
        #region _ILyncClientEvents support
        public event _ILyncClientEvents_OnStateChangedEventHandler OnStateChanged;
        public event _ILyncClientEvents_OnNotificationReceivedEventHandler OnNotificationReceived;
        public event _ILyncClientEvents_OnCredentialRequestedEventHandler OnCredentialRequested;
        public event _ILyncClientEvents_OnSignInDelayedEventHandler OnSignInDelayed;
        public event _ILyncClientEvents_OnCapabilitiesChangedEventHandler OnCapabilitiesChanged;
        public event _ILyncClientEvents_OnDelegatorClientAddedEventHandler OnDelegatorClientAdded;
        public event _ILyncClientEvents_OnDelegatorClientRemovedEventHandler OnDelegatorClientRemoved;
        // Notifies Office apps that the IM client state (signed out, signing in, singed in, signing out, etc) has changed.
        internal void RaiseOnStateChangedEvent(ClientStateChangedEventData eventData)
        {
            if (this.OnStateChanged != null)
            {
                this.OnStateChanged(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a notification event from MAPI (e.g. autodiscover has finished)
        internal void RaiseOnNotificationReceivedEvent(LyncClientNotificationReceivedEventData eventData)
        {
            if (this.OnNotificationReceived != null)
            {
                this.OnNotificationReceived(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a request for credentials for some operation (e.g. sign in, web search)
        internal void RaiseOnCredentialRequestedEvent(CredentialRequestedEventData eventData)
        {
            if (this.OnCredentialRequested != null)
            {
                this.OnCredentialRequested(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has been delayed from signing in and gives an estimated delay time.
        internal void RaiseOnSignInDelayedEvent(SignInDelayedEventData eventData)
        {
            if (this.OnSignInDelayed != null)
            {
                this.OnSignInDelayed(this, eventData);
            }
        }
        // Notifies Office apps that the capabilities of this IM client have changed.
        internal void RaiseOnCapabilitiesChangedEvent(PreferredCapabilitiesChangedEventData eventData)
        {
            if (this.OnCapabilitiesChanged != null)
            {
                this.OnCapabilitiesChanged(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been added to the IM client object.
        internal void RaiseOnDelegatorClientAdded(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientAdded != null)
            {
                this.OnDelegatorClientAdded(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been removed from the IM client object.
        internal void RaiseOnDelegatorClientRemoved(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientRemoved != null)
            {
                this.OnDelegatorClientRemoved(this, eventData);
            }
        }
        #endregion
    }
}
```

### <a name="iautomation-interface"></a><span data-ttu-id="30a0d-343">Interface IAutomation</span><span class="sxs-lookup"><span data-stu-id="30a0d-343">IAutomation interface</span></span>
<span data-ttu-id="30a0d-344"><a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-344"></span></span>

<span data-ttu-id="30a0d-p130">L'interface **IAutomation** automatise les fonctionnalités de l'application cliente de messagerie instantanée. Elle peut être utilisée pour démarrer une conversation, participer à des conférences et fournir un contexte de fenêtre d'extensibilité.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p130">The **IAutomation** interface automates features of the IM client application. It can be used to start conversations, join conferences, and provide extensibility window context.</span></span> 
  
<span data-ttu-id="30a0d-347">Le tableau 4 indique les membres qui doivent être implémentés dans la classe qui hérite de **IAutomation**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-347">Table 4 shows the members that must be implemented in the class that inherits from **IAutomation**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="30a0d-348">Tout membre de l'interface **IAutomation** non répertorié dans le tableau doit être présent, mais ne doit pas nécessairement être implémenté.</span><span class="sxs-lookup"><span data-stu-id="30a0d-348">Any member of the **IAutomation** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="30a0d-349">Les membres présents, mais non implémentés, peuvent générer une erreur**NotImplementedException** ou **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-349">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="30a0d-350">Pour plus d'informations sur l'interface **IAutomation** et ses membres, consultez [UCCollaborationLib.IAutomation](http://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span><span class="sxs-lookup"><span data-stu-id="30a0d-350">> For more information about the **IAutomation** interface and its members, see [UCCollaborationLib.IAutomation](http://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span></span> 
  
<span data-ttu-id="30a0d-351">**Tableau 4. Implémentation de l’interface IAutomation**</span><span class="sxs-lookup"><span data-stu-id="30a0d-351">**Table 4. Implementation of IAutomation interface**</span></span>

|<span data-ttu-id="30a0d-352">**Membre**</span><span class="sxs-lookup"><span data-stu-id="30a0d-352">**Member**</span></span>|<span data-ttu-id="30a0d-353">**Description**</span><span class="sxs-lookup"><span data-stu-id="30a0d-353">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30a0d-354">Méthode **StartConversation**</span><span class="sxs-lookup"><span data-stu-id="30a0d-354">**StartConversation** method</span></span>  <br/> |<span data-ttu-id="30a0d-p132">Démarre une conversation à l'aide de la modalité de conversation spécifiée. Une instance de **IConversationWindow** est renvoyée.  </span><span class="sxs-lookup"><span data-stu-id="30a0d-p132">Starts a conversation using the specified conversation modality. An instance of **IConversationWindow** is returned.  </span></span><br/> |
   
## <a name="implementing-contact-presence-integration"></a><span data-ttu-id="30a0d-357">Implémentation de l’intégration de la présence du contact</span><span class="sxs-lookup"><span data-stu-id="30a0d-357">Implementing contact presence integration</span></span>
<span data-ttu-id="30a0d-358"><a name="off15_IMIntegration_ImplementIMFeatures"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-358"></span></span>

<span data-ttu-id="30a0d-p133">En plus des trois interfaces requises mentionnées précédemment, il existe plusieurs autres interfaces importantes pour l’activation des fonctionnalités de la présence du contact dans Office. En voici quelques-unes :</span><span class="sxs-lookup"><span data-stu-id="30a0d-p133">In addition to the three required interfaces discussed previously, there are several other interfaces that are important for enabling contact presence functionality in Office. These include the following:</span></span>
  
- <span data-ttu-id="30a0d-361">Interface [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) ou **IContact2**</span><span class="sxs-lookup"><span data-stu-id="30a0d-361">The [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) or **IContact2** interface.</span></span> 
    
- <span data-ttu-id="30a0d-362">Interface [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf)</span><span class="sxs-lookup"><span data-stu-id="30a0d-362">The [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) interface.</span></span> 
    
- <span data-ttu-id="30a0d-363">Interfaces [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) et [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager)</span><span class="sxs-lookup"><span data-stu-id="30a0d-363">The [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) and [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) interfaces.</span></span> 
    
- <span data-ttu-id="30a0d-364">Interfaces [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) et [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup)</span><span class="sxs-lookup"><span data-stu-id="30a0d-364">The [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) and [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) interfaces.</span></span> 
    
- <span data-ttu-id="30a0d-365">Interface [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription)</span><span class="sxs-lookup"><span data-stu-id="30a0d-365">The [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) interface.</span></span> 
    
- <span data-ttu-id="30a0d-366">Interface [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint)</span><span class="sxs-lookup"><span data-stu-id="30a0d-366">The [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) interface.</span></span> 
    
- <span data-ttu-id="30a0d-367">Interface [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString)</span><span class="sxs-lookup"><span data-stu-id="30a0d-367">The [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) interface</span></span> 
    
### <a name="icontact-interface"></a><span data-ttu-id="30a0d-368">Interface IContact</span><span class="sxs-lookup"><span data-stu-id="30a0d-368">IContact interface</span></span>
<span data-ttu-id="30a0d-369"><a name="off15_IMIntegration_ImplementRequired_IContact"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-369"></span></span>

<span data-ttu-id="30a0d-p134">L'interface **IContact** représente un utilisateur de l'application cliente de messagerie instantanée. L'interface expose la présence, les modalités disponibles, l'appartenance à un groupe et les propriétés du type de contact d'un utilisateur. Pour démarrer une conversation avec un autre utilisateur, vous devez fournir cette instance d'utilisateur **IContact**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p134">The **IContact** interface represents an IM client application user. The interface exposes presence, available modalities, group membership, and contact type properties for a user. To start a conversation with another user, you must provide that user instance of **IContact**.</span></span>
  
<span data-ttu-id="30a0d-373">Le tableau 5 indique les membres qui doivent être implémentés dans la classe qui hérite de **IContact**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-373">Table 5 shows the members that must be implemented in the class that inherits from **IContact**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="30a0d-374">Tout membre de l'interface **IContact** non répertorié dans le tableau doit être présent, mais ne doit pas nécessairement être implémenté.</span><span class="sxs-lookup"><span data-stu-id="30a0d-374">Any member of the **IContact** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="30a0d-375">Les membres présents, mais non implémentés, peuvent générer une erreur**NotImplementedException** ou **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-375">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="30a0d-376">Pour plus d'informations sur l'interface **IContact** et ses membres, consultez [UCCollaborationLib.IContact](http://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span><span class="sxs-lookup"><span data-stu-id="30a0d-376">> For more information about the **IContact** interface and its members, see [UCCollaborationLib.IContact](http://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span></span> 
  
<span data-ttu-id="30a0d-377">**Tableau 5. Implémentation de l’interface IContact**</span><span class="sxs-lookup"><span data-stu-id="30a0d-377">**Table 5. Implementation of the IContact interface**</span></span>

|<span data-ttu-id="30a0d-378">**Membre**</span><span class="sxs-lookup"><span data-stu-id="30a0d-378">**Member**</span></span>|<span data-ttu-id="30a0d-379">**Description**</span><span class="sxs-lookup"><span data-stu-id="30a0d-379">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30a0d-380">Méthode **CanStart**</span><span class="sxs-lookup"><span data-stu-id="30a0d-380">**CanStart** method</span></span>  <br/> |<span data-ttu-id="30a0d-381">Renvoie **true** si un type de modalité donné peut être démarré sur le contact.</span><span class="sxs-lookup"><span data-stu-id="30a0d-381">Returns **true** if a given type of modality can be started on the contact.</span></span>  <br/> |
|<span data-ttu-id="30a0d-382">Méthode **GetContactInformation**</span><span class="sxs-lookup"><span data-stu-id="30a0d-382">**GetContactInformation** method</span></span>  <br/> |<span data-ttu-id="30a0d-383">Obtient un élément de présence à partir d’un contact de publication.</span><span class="sxs-lookup"><span data-stu-id="30a0d-383">Gets one presence item from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="30a0d-384">Méthode **BatchGetContactInformation**</span><span class="sxs-lookup"><span data-stu-id="30a0d-384">**BatchGetContactInformation** method</span></span>  <br/> |<span data-ttu-id="30a0d-385">Obtient plusieurs éléments de présence à partir d’un contact de publication.</span><span class="sxs-lookup"><span data-stu-id="30a0d-385">Gets multiple presence items from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="30a0d-386">Propriété **Settings**</span><span class="sxs-lookup"><span data-stu-id="30a0d-386">**Settings** property</span></span>  <br/> |<span data-ttu-id="30a0d-387">Obtient une collection de propriétés de contact.</span><span class="sxs-lookup"><span data-stu-id="30a0d-387">Gets a collection of contact properties.</span></span>  <br/> |
|<span data-ttu-id="30a0d-388">Propriété **CustomGroups**</span><span class="sxs-lookup"><span data-stu-id="30a0d-388">**CustomGroups** property</span></span>  <br/> |<span data-ttu-id="30a0d-389">Obtient une collection de groupes dont le contact est membre.</span><span class="sxs-lookup"><span data-stu-id="30a0d-389">Gets a collection of groups that the contact is a member of.</span></span>  <br/> |
   
<span data-ttu-id="30a0d-p136">Pendant le processus d'initialisation, l'application Office appelle la méthode **IContact.CanStart** pour déterminer les fonctionnalités de messagerie instantanée de l'utilisateur local. La méthode **CanStart** récupère un indicateur à partir de l'énumération [UCCollaborationLib.ModalityTypes](http://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) en tant qu'argument pour le paramètre  __modalityTypes_. Si l'utilisateur peut participer à la modalité demandée (autrement dit, si l'utilisateur est capable d'utiliser la messagerie instantanée, la messagerie audio et vidéo ou le partage d'application), la méthode **CanStart** renvoie **true**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p136">During the initialization process, the Office application calls the **IContact.CanStart** method to determine the IM capabilities for the local user. The **CanStart** method takes a flag from the [UCCollaborationLib.ModalityTypes](http://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) enumeration as an argument for the  __modalityTypes_ parameter. If the current user can engage in the requested modality (that is, the user is capable of instant messaging, audio and video messaging, or application sharing), the **CanStart** method returns **true**.</span></span>
  
```cs
public bool CanStart(ModalityTypes _modalityTypes)
{
    // Define the capabilities of the current IM client application
    // user by using flags from the ModalityTypes enumeration.
    ModalityTypes userCapabilities = 
        ModalityTypes.ucModalityInstantMessage | 
        ModalityTypes.ucModalityAudioVideo | 
        ModalityTypes.ucModalityAppSharing;
    // Perform a simple test for equivalency.
    if (_modalityType == userCapabilities) 
    {
        return true;
    }
    else 
    {
        return false;
    }
}

```

<span data-ttu-id="30a0d-p137">La méthode **GetContactInformation** récupère les informations relatives au contact à partir de l'objet **IContact**. Le code appelant doit transmettre une valeur à partir de l'énumération [UCCollaborationLib.ContactInformationType](http://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) pour le paramètre  __contactInformationType_, qui indique les données à récupérer.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p137">The **GetContactInformation** method retrieves information about the contact from the **IContact** object. The calling code needs to pass in a value from the [UCCollaborationLib.ContactInformationType](http://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) enumeration for the  __contactInformationType_ parameter, which indicates the data to be retrieved.</span></span> 
  
```cs
public object GetContactInformation(
    ContactInformationType _contactInformationType)
{
    // Determine the information to return from the contact's data based
    // on the value passed in for the _contactInformationType parameter.
    switch (_contactInformationType)
    {
        case ContactInformationType.ucPresenceEmailAddresses:
        {
            // Return the URI associated with the contact.
            string returnValue = this.Uri.ToLower().Replace("sip:", String.Empty);
            return returnValue;
        }
        case ContactInformationType.ucPresenceDisplayName:
        {
            // Return the display name associated with the contact.
            string returnValue = this._DisplayName;
            return returnValue;
        }
        default:
        {
            throw new NotImplementedException;
        }
        // Additional implementation details omitted.
    }
}
```

<span data-ttu-id="30a0d-p138">Similaire à **GetContactInformation**, la méthode **BatchGetContactInformation** extrait plusieurs éléments de présence relatifs au contact à partir de l'objet **IContact**. Le code appelant doit transmettre un tableau de valeurs à partir de l'énumération **ContactInformationType** pour le paramètre  __contactInformationTypes_. La méthode renvoie un objet [UCCollaborationLib.IContactInformationDictionary](http://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) contenant les données requises.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p138">Similar to the **GetContactInformation**, the **BatchGetContactInformation** method retrieves multiple presence items about the contact from the **IContact** object. The calling code needs to pass in an array of values from the **ContactInformationType** enumeration for the  __contactInformationTypes_ parameter. The method returns an [UCCollaborationLib.IContactInformationDictionary](http://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) object that contains the requested data.</span></span> 
  
```cs
public IMClientContactInformationDictionary BatchGetContactInformation(
    ContactInformationType[] _contactInformationTypes)
{
    // The IMClientContactInformationDictionary class implements the
    // IContactInformationDictionary interface.
    IMClientContactInformationDictionary contactDictionary = 
        new IMClientContactInformationDictionary();
    foreach (ContactInformationType type in _contactInformationTypes)
    {
        // Call GetContactInformation for each type of contact 
        // information to retrieve. This code adds a new entry to
        // a Dictionary object exposed by the
        // ContactInformationDictionary property.
        contactDictionary.ContactInformationDictionary.Add(
            type, this.GetContactInformation(type));
    }
    return contactDictionary;
}
```

<span data-ttu-id="30a0d-398">La propriété **IContact.Settings** renvoie un objet **IContactSettingDictionary** contenant les propriétés personnalisées relatives au contact.</span><span class="sxs-lookup"><span data-stu-id="30a0d-398">The **IContact.Settings** property returns an **IContactSettingDictionary** object that contains custom properties about the contact.</span></span> 
  
```cs
public IMClientContactSettingDictionary Settings
{
    get
    {
       // The IMClientContactSettingDictionary class implements
       // the IContactSettingDictionary interface.
       return new IMClientContactSettingDictionary();
    }
}
```

<span data-ttu-id="30a0d-399">La propriété **IContact.CustomGroups** renvoie un objet **IGroupCollection** incluant tous les groupes dont le contact est membre.</span><span class="sxs-lookup"><span data-stu-id="30a0d-399">The **IContact.CustomGroups** property returns an **IGroupCollection** object that includes all of the groups of which the contact is a member.</span></span> 
  
```cs
public IMClientGroupCollection CustomGroups
{
    get {
       // The IMClientGroupCollection class implements
       // the IGroupCollection interface.
        return new IMClientGroupCollection();
    }
}
```

### <a name="iself-interface"></a><span data-ttu-id="30a0d-400">Interface ISelf</span><span class="sxs-lookup"><span data-stu-id="30a0d-400">ISelf interface</span></span>
<span data-ttu-id="30a0d-401"><a name="off15_IMIntegration_ImplementRequired_ISelf"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-401"></span></span>

<span data-ttu-id="30a0d-p139">Pendant le processus d'initialisation, l'application Office récupère les données de l'utilisateur actuel en accédant à la propriété **ILyncClient.Self**, qui doit renvoyer un objet **ISelf**. L'interface **ISelf** représente l'utilisateur local et connecté de l'application cliente de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p139">During the initialization process, the Office application gets the data for the current user by accessing the **ILyncClient.Self** property, which must return an **ISelf** object. The **ISelf** interface represents the local, signed-in IM client application user.</span></span> 
  
<span data-ttu-id="30a0d-404">Le tableau 6 présente les membres qui doivent être implémentés dans la classe qui hérite de **ISelf**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-404">Table 6 shows the members that must be implemented in the class that inherits from **ISelf**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="30a0d-p140">Tout membre de l'interface **ISelf** non répertorié dans le tableau doit être présent, mais ne doit pas nécessairement être implémenté. Les membres présents, mais non implémentés, peuvent lever une erreur **NotImplementedException** ou **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p140">Any member of the **ISelf** interface not listed in the table must be present but does not need to be implemented. Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
  
<span data-ttu-id="30a0d-407">**Tableau 6. Implémentation de l'interface ISelf**</span><span class="sxs-lookup"><span data-stu-id="30a0d-407">**Table 6. Implementation of the ISelf interface**</span></span>

|<span data-ttu-id="30a0d-408">**Membre**</span><span class="sxs-lookup"><span data-stu-id="30a0d-408">**Member**</span></span>|<span data-ttu-id="30a0d-409">**Description**</span><span class="sxs-lookup"><span data-stu-id="30a0d-409">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30a0d-410">Propriété **Contact**</span><span class="sxs-lookup"><span data-stu-id="30a0d-410">**Contact** property</span></span>  <br/> |<span data-ttu-id="30a0d-411">Obtient l'objet **IContact** associé à l'utilisateur local.</span><span class="sxs-lookup"><span data-stu-id="30a0d-411">Gets the **IContact** object associated with the local user.</span></span>  <br/> |
   
<span data-ttu-id="30a0d-p141">Les propriétés de présence, de modalités disponibles, d'appartenance au groupe et de type de contact de l'utilisateur local sont exposées via la propriété **ISelf.Contact** (qui renvoie un objet **IContact**). Pendant le processus d'initialisation, l'application Office accède à la propriété **ISelf.Contact** pour obtenir une référence aux informations de contact de l'utilisateur local.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p141">Presence, available modalities, group membership, and contact type properties for the local user are exposed through the **ISelf.Contact** property (which returns an **IContact** object). During the initialization process, the Office application accesses the **ISelf.Contact** property to get a reference to the contact information for the local user.</span></span> 
  
<span data-ttu-id="30a0d-414">Utilisez le code suivant pour définir une classe qui hérite de l'interface **ISelf** qui implémente la propriété **Contact**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-414">Use the following code to define a class that inherits from the **ISelf** interface that implements the **Contact** property.</span></span> 
  
```cs
[ComVisible(true)]
public class IMClientSelf : ISelf
{
    // Declare a private field to store contact data for local user.
    private IMClientContact _contactData;
    // In the constructor for the ISelf object, the calling code 
    // must supply contact data.
    public IMClientSelf (IMClientContact _selfContactData)
    {
        this._contactData = _selfContactData;
    }
    // When accessed, the Contact property returns a reference
    // to the IContact object that represents the local user.
    public IMClientContact Contact
    {
        get
        {
            return this._contactData as IMClientContact;
        }
    }
    // Additional implementation details omitted.
}
```

### <a name="icontactmanager-and-icontactmanagerevents-interfaces"></a><span data-ttu-id="30a0d-415">Interfaces IContactManager et _IContactManagerEvents</span><span class="sxs-lookup"><span data-stu-id="30a0d-415">IContactManager and _IContactManagerEvents interfaces</span></span>
<span data-ttu-id="30a0d-416"><a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-416"></span></span>

<span data-ttu-id="30a0d-p142">L'objet **IContactManager** gère les contacts de l'utilisateur local, notamment les informations de contact de cet utilisateur local. L'application Office utilise un objet **IContactManager** pour accéder aux objets **IContact** qui correspondent aux contacts de l'utilisateur local.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p142">The **IContactManager** object manages the contacts for the local user, including the local user's own contact information. The Office application uses an **IContactManager** object to access **IContact** objects that correspond to the local user's contacts.</span></span> 
  
<span data-ttu-id="30a0d-419">Le tableau 7 affiche les membres qui doivent être implémentés dans la classe qui hérite de **IContactManager** et **_IContactManagerEvents**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-419">Table 7 shows the members that must be implemented in the class that inherits from **IContactManager** and **_IContactManagerEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="30a0d-420">Tout membre de l’interface **IContactManager** non répertorié dans le tableau doit être présent, mais ne doit pas nécessairement être implémenté.</span><span class="sxs-lookup"><span data-stu-id="30a0d-420">Any member of the **IContactManager** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="30a0d-421">Les membres présents, mais non implémentés, peuvent générer une erreur **NotImplementedException** ou **E\_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-421">Members that are present but not implemented can throw a NotImplementedException or E_NOTIMPL error.</span></span> 
>
> <span data-ttu-id="30a0d-422">Pour plus d'informations sur les interfaces **IContactManager** et **_IContactManagerEvents**, ainsi que sur leurs membres, consultez [UCCollaborationLib.IContactManager](http://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) et [UCCollaborationLib._IContactManagerEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span><span class="sxs-lookup"><span data-stu-id="30a0d-422">> For more information about the **IContactManager** and **_IContactManagerEvents** interfaces and their members, see [UCCollaborationLib.IContactManager](http://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) and [UCCollaborationLib._IContactManagerEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span></span> 
  
<span data-ttu-id="30a0d-423">**Tableau 7. Implémentation des interfaces IContactManager et _IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="30a0d-423">**Table 7. Implementation of the IContactManager and _IContactManagerEvents interfaces**</span></span>

|<span data-ttu-id="30a0d-424">**Interface**</span><span class="sxs-lookup"><span data-stu-id="30a0d-424">**Interface**</span></span>|<span data-ttu-id="30a0d-425">**Membre**</span><span class="sxs-lookup"><span data-stu-id="30a0d-425">**Member**</span></span>|<span data-ttu-id="30a0d-426">**Description**</span><span class="sxs-lookup"><span data-stu-id="30a0d-426">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30a0d-427">**IContactManager**</span><span class="sxs-lookup"><span data-stu-id="30a0d-427">**IContactManager**</span></span> <br/> |<span data-ttu-id="30a0d-428">Méthode **GetContactByUri**</span><span class="sxs-lookup"><span data-stu-id="30a0d-428">**GetContactByUri** method</span></span>  <br/> |<span data-ttu-id="30a0d-429">Recherche ou crée une instance de contact à l’aide de l’URI du contact.</span><span class="sxs-lookup"><span data-stu-id="30a0d-429">Finds or creates a new contact instance by using the contact URI.</span></span>  <br/> |
||<span data-ttu-id="30a0d-430">Méthode **CreateSubscription**</span><span class="sxs-lookup"><span data-stu-id="30a0d-430">**CreateSubscription** method</span></span>  <br/> |<span data-ttu-id="30a0d-431">Crée un objet **ISubscription** qui peut être utilisé pour le traitement par lots des abonnements ou des requêtes.</span><span class="sxs-lookup"><span data-stu-id="30a0d-431">Creates an **ISubscription** object that can be used for batching subscriptions or queries.</span></span>  <br/> |
||<span data-ttu-id="30a0d-432">Méthode **Lookup**</span><span class="sxs-lookup"><span data-stu-id="30a0d-432">**Lookup** method</span></span>  <br/> |<span data-ttu-id="30a0d-433">Recherche un groupe de contacts ou de distribution.</span><span class="sxs-lookup"><span data-stu-id="30a0d-433">Looks up a contact or distribution group.</span></span>  <br/> |
|<span data-ttu-id="30a0d-434">**_IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="30a0d-434">**_IContactManagerEvents**</span></span> <br/> |<span data-ttu-id="30a0d-435">Événement **OnGroupAdded**</span><span class="sxs-lookup"><span data-stu-id="30a0d-435">**OnGroupAdded** event</span></span>  <br/> |<span data-ttu-id="30a0d-p144">Déclenché lorsqu'un groupe est ajouté à une collection de groupes. La collection de groupes mise à jour peut être obtenue à partir de la propriété **IContactManager.Groups**.  </span><span class="sxs-lookup"><span data-stu-id="30a0d-p144">Raised when a group is added to a group collection. The updated group collection can be obtained from the **IContactManager.Groups** property.  </span></span><br/> |
||<span data-ttu-id="30a0d-438">Événement **OnGroupRemoved**</span><span class="sxs-lookup"><span data-stu-id="30a0d-438">**OnGroupRemoved** event</span></span>  <br/> |<span data-ttu-id="30a0d-p145">Déclenché lorsqu'un groupe est supprimé d'une collection de groupes. La collection de groupes mise à jour peut être obtenue à partir de la propriété **IContactManager.Groups**.  </span><span class="sxs-lookup"><span data-stu-id="30a0d-p145">Raised when a group is removed from a group collection. The updated group collection can be obtained from the **IContactManager.Groups** property.  </span></span><br/> |
||<span data-ttu-id="30a0d-441">Événement **OnSearchProviderStateChanged**</span><span class="sxs-lookup"><span data-stu-id="30a0d-441">**OnSearchProviderStateChanged** event</span></span>  <br/> |<span data-ttu-id="30a0d-442">Déclenché lorsque le statut d’un fournisseur de recherche change.</span><span class="sxs-lookup"><span data-stu-id="30a0d-442">Raised when a search provider's status changes.</span></span>  <br/> |
   
<span data-ttu-id="30a0d-p146">Office appelle **IContactManager.GetContactByUri** pour obtenir les informations de présence d'un contact à l'aide de son adresse SIP. Lorsqu'un contact est configuré pour une adresse SIP dans Active Directory, Office détermine cette adresse pour un contact et appelle **GetContactByUri**, transmettant l'adresse SIP du contact vers le paramètre  __contactUri_.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p146">Office calls **IContactManager.GetContactByUri** to get a contact's presence information, by using the SIP address of the contact. When a contact is configured for an SIP address in the Active Directory, Office determines this address for a contact and calls **GetContactByUri**, passing the SIP address of the contact in for the  __contactUri_ parameter.</span></span> 
  
<span data-ttu-id="30a0d-p147">Lorsqu'Office ne peut pas déterminer l'adresse SIP du contact, il appelle la méthode **IContactManager.Lookup** pour trouver le SIP en utilisant le service de messagerie instantanée. Ici, Office transmet les meilleures données du contact qu'il peut trouver (par exemple, seule l'adresse de messagerie du contact). La méthode **Lookup** renvoie de manière asynchrone un objet **AsynchronousOperation**. Lorsqu'elle appelle le rappel, la méthode **Lookup** doit renvoyer la réussite ou l'échec de l'opération en plus de l'URI du contact.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p147">When Office cannot determine the SIP address for the contact, it calls the **IContactManager.Lookup** method to find the SIP by using the IM service. Here Office passes in the best data that it can find for the contact (for example, just the email address for the contact). The **Lookup** method asynchronously returns an **AsynchronousOperation** object. When it invokes the callback, the **Lookup** method should return the success or failure of the operation in addition to the URI of the contact.</span></span> 
  
```cs
public IMClientContact GetContactByUri(string _contactUri)
{
    // Declare a Contact variable to contain information about the contact.
    IMClientContact tempContact = null;
    // The _groupCollections field is an IGroupCollection object. Iterate 
    // over each group in collection to see if the 
    // contact is a part of the group.
    foreach (IMClientGroup group in this._groupCollections)
    {
       if (group.TryGetContact(_contactUri, out tempContact))
       {
           break;
       }
    }
    // Check to see that the URI returned a valid contact. If it
    // did not, create a new contact.
    if (tempContact == null)
    {
        tempContact = IMClientContact.BuildContact(_contactUri);
    }
    // Return the contact to the calling code.
    return tempContact;
}
```

<span data-ttu-id="30a0d-p148">L'application Office doit s'abonner aux modifications de présence d'un contact individuel. Par conséquent, lorsque le statut de présence d'un contact change, le serveur de messagerie instantanée avertit l'application cliente de messagerie instantanée, ce qui permet d'alerter l'application Office. Pour ce faire, l'application Office appelle la méthode **IContactManager.CreateSubscription** pour créer un objet **IContactSubscription** pour cette requête.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p148">The Office application needs to subscribe to presence changes for an individual contact. Thus, when a contact's presence status changes, the IM server alerts the IM client application—thereby alerting the Office application. To do this, the Office application calls the **IContactManager.CreateSubscription** method to create a new **IContactSubscription** object for this request.</span></span> 
  
```cs
// Declare a private field to contain an IContactSubscription object.
private IMClientContactSubscription _contactSubscription;
// Return the IContactSubscription object associated 
// with the IContactManager object.
public IMClientContactSubscription CreateSubscription()
{
    return this._contactSubscription;
}
```

### <a name="igroup-and-igroupcollection-interfaces"></a><span data-ttu-id="30a0d-452">Interfaces IGroup et IGroupCollection</span><span class="sxs-lookup"><span data-stu-id="30a0d-452">IGroup and IGroupCollection interfaces</span></span>
<span data-ttu-id="30a0d-453"><a name="off15_IMIntegration_ImplementRequired_IGroup"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-453"></span></span>

<span data-ttu-id="30a0d-p149">L'objet **IGroup** représente un ensemble de contacts avec des propriétés supplémentaires pour l'identification d'une collection de contacts par un nom de groupe collectif. Un objet **IGroupCollection** représente une collection d'objets **IGroup** définis par un utilisateur local et l'application cliente de messagerie instantanée. L'application Office utilise les objets **IGroupCollection** et **IGroup** pour accéder aux contacts de l'utilisateur local.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p149">The **IGroup** object represents a collection of contacts with additional properties for identifying the contact collection by a collective group name. An **IGroupCollection** object represents a collection of **IGroup** objects defined by a local user and the IM client application. The Office application uses the **IGroupCollection** and **IGroup** objects to access the local user's contacts.</span></span> 
  
<span data-ttu-id="30a0d-457">Le tableau 9 affiche les membres qui doivent être implémentés dans les classes qui héritent de **IGroup** et **IGroupCollection** dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="30a0d-457">Table 9 shows the members that must be implemented in the classes that inherit from **IGroup** and **IGroupCollection** in the following table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="30a0d-458">Tout membre de l'interface **IGroup** non répertorié dans le tableau doit être présent, mais ne doit pas nécessairement être implémenté.</span><span class="sxs-lookup"><span data-stu-id="30a0d-458">Any member of the **IGroup** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="30a0d-459">Les membres présents, mais non implémentés, peuvent générer une erreur**NotImplementedException** ou **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-459">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="30a0d-460">Pour plus d'informations sur les interfaces **IGroup** et **IGroupCollection**, ainsi que sur leurs membres, consultez [UCCollaborationLib.IGroup](http://msdn.microsoft.com/library/UCCollaborationLib.IGroup) et [UCCollaborationLib.IGroupCollection](http://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span><span class="sxs-lookup"><span data-stu-id="30a0d-460">> For more information about the **IGroup** and **IGroupCollection** interfaces and their members, see [UCCollaborationLib.IGroup](http://msdn.microsoft.com/library/UCCollaborationLib.IGroup) and [UCCollaborationLib.IGroupCollection](http://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span></span> 
  
<span data-ttu-id="30a0d-461">**Tableau 9. Implémentation des interfaces IGroup et IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="30a0d-461">**Table 9. Implementation of the IGroup and IGroupCollection interfaces**</span></span>

|<span data-ttu-id="30a0d-462">**Interface**</span><span class="sxs-lookup"><span data-stu-id="30a0d-462">**Interface**</span></span>|<span data-ttu-id="30a0d-463">**Membre**</span><span class="sxs-lookup"><span data-stu-id="30a0d-463">**Member**</span></span>|<span data-ttu-id="30a0d-464">**Description**</span><span class="sxs-lookup"><span data-stu-id="30a0d-464">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30a0d-465">**IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="30a0d-465">**IGroupCollection**</span></span> <br/> |<span data-ttu-id="30a0d-466">Propriété **Count**</span><span class="sxs-lookup"><span data-stu-id="30a0d-466">**Count** property</span></span>  <br/> |<span data-ttu-id="30a0d-467">Renvoie le nombre d'objets **IGroup** de la collection.</span><span class="sxs-lookup"><span data-stu-id="30a0d-467">Returns the count of **IGroup** objects in the collection</span></span>  <br/> |
||<span data-ttu-id="30a0d-468">Propriété **Item**</span><span class="sxs-lookup"><span data-stu-id="30a0d-468">**Item** property</span></span>  <br/> |<span data-ttu-id="30a0d-469">Renvoie l'objet **IGroup** à la position d'index de la collection.</span><span class="sxs-lookup"><span data-stu-id="30a0d-469">Returns the **IGroup** object at the specified index in the collection.</span></span>  <br/> |
|<span data-ttu-id="30a0d-470">**IGroup**</span><span class="sxs-lookup"><span data-stu-id="30a0d-470">**IGroup**</span></span> <br/> |<span data-ttu-id="30a0d-471">Propriété **Id**</span><span class="sxs-lookup"><span data-stu-id="30a0d-471">**Id** property</span></span>  <br/> |<span data-ttu-id="30a0d-472">Renvoie l’ID du groupe.</span><span class="sxs-lookup"><span data-stu-id="30a0d-472">Returns the ID of the group.</span></span>  <br/> |
   
<span data-ttu-id="30a0d-p151">Lorsque l'application Office obtient les informations relatives à l'utilisateur local, elle accède à l'appartenance aux groupes du contact (utilisateur local) en appelant la propriété **IContact.CustomGroups**, qui renvoie un objet **IGroupCollection**. Le **IGroupCollection** doit contenir un tableau (ou **List**) des objets **IGroup**. La classe qui dérive de **IGroupCollection** doit exposer une propriété **Count**, qui renvoie le nombre d'éléments de la collection, ainsi qu'une méthode d'indexation, **this(int)**, qui renvoie un objet **IGroup** à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p151">When the Office application gets the information for the local user, it accesses the group memberships of the contact (local user) by calling the **IContact.CustomGroups** property, which returns an **IGroupCollection** object. The **IGroupCollection** must contain an array (or **List**) of **IGroup** objects. The class that derives from **IGroupCollection** must expose a **Count** property, which returns the number of items in the collection, and an indexer method, **this(int)**, which returns an **IGroup** object from the collection.</span></span> 
  
### <a name="icontactsubscription-interface"></a><span data-ttu-id="30a0d-476">Interface IContactSubscription</span><span class="sxs-lookup"><span data-stu-id="30a0d-476">IContactSubscription interface</span></span>
<span data-ttu-id="30a0d-477"><a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-477"></span></span>

<span data-ttu-id="30a0d-p152">L'interface **IContactSubscription** vous permet de spécifier des contacts dont vous souhaitez recevoir des mises à jour d'informations de présence, ainsi que les types d'informations de présence qui déclenchent l'envoi d'une notification. Les applications Office utilisent un objet **IContactSubscription** pour enregistrer les modifications apportées au statut de présence du contact.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p152">The **IContactSubscription** interface allows you to specify the contacts to receive presence information updates for and the types of presence information that trigger a notification. Office applications use an **IContactSubscription** object to register changes to contact's presence status.</span></span> 
  
<span data-ttu-id="30a0d-480">Le tableau 10 indique les membres qui doivent être implémentés dans les classes qui héritent de **IContactSubscription**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-480">Table 10 shows the members that must be implemented in the classes that inherit from **IContactSubscription**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="30a0d-481">Tout membre de l'interface **IContactSubscription** non répertorié dans le tableau doit être présent, mais ne doit pas nécessairement être implémenté.</span><span class="sxs-lookup"><span data-stu-id="30a0d-481">Any member of the **IContactSubscription** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="30a0d-482">Les membres présents, mais non implémentés, peuvent générer une erreur**NotImplementedException** ou **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-482">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="30a0d-483">Pour plus d'informations sur l'interface **IContactSubscription** et ses membres, consultez [UCCollaborationLib.IContactSubscription](http://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span><span class="sxs-lookup"><span data-stu-id="30a0d-483">> For more information about the **IContactSubscription** interface and its members, see [UCCollaborationLib.IContactSubscription](http://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span></span> 
  
<span data-ttu-id="30a0d-484">**Tableau 10. Implémentation de l’interface IContactSubscription**</span><span class="sxs-lookup"><span data-stu-id="30a0d-484">**Table 10. Implementation of the IContactSubscription interface**</span></span>

|<span data-ttu-id="30a0d-485">**Membre**</span><span class="sxs-lookup"><span data-stu-id="30a0d-485">**Member**</span></span>|<span data-ttu-id="30a0d-486">**Description**</span><span class="sxs-lookup"><span data-stu-id="30a0d-486">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30a0d-487">Méthode **AddContact**</span><span class="sxs-lookup"><span data-stu-id="30a0d-487">**AddContact** method</span></span>  <br/> |<span data-ttu-id="30a0d-488">Ajoute un contact à l’objet d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="30a0d-488">Adds a contact to the subscription object.</span></span>  <br/> |
|<span data-ttu-id="30a0d-489">Méthode **Subscribe**</span><span class="sxs-lookup"><span data-stu-id="30a0d-489">**Subscribe** method</span></span>  <br/> |<span data-ttu-id="30a0d-490">Permet à l’application cliente de messagerie instantanée de suivre la présence d’un contact.</span><span class="sxs-lookup"><span data-stu-id="30a0d-490">Helps the IM client application to monitor presence for a contact.</span></span>  <br/> |
   
<span data-ttu-id="30a0d-p154">L'interface **IContactSubscription** doit contenir une référence pointant vers tous les objets **IContact** qu'elle surveille, à l'aide d'un tableau ou d'une **List**. La méthode **IContactSubscription.AddContact** ajoute un objet **IContact** pour la structure de données sous-jacente de l'objet **IContactSubscription**, ce qui ajoute un nouveau contact dont les changements de présence doivent être suivis.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p154">The **IContactSubscription** interface must contain a reference to all the **IContact** objects that it monitors, using an array or a **List**. The **IContactSubscription.AddContact** method adds an **IContact** object for the to the underlying data structure of the **IContactSubscription** object, thereby adding a new contact to monitor for presence changes.</span></span> 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

<span data-ttu-id="30a0d-p155">La méthode **IContactSubscription.Subscribe** permet à une application cliente de messagerie instantanée d'accéder aux observateurs de présence du contact. Elle peut utiliser une stratégie d'interrogation pour obtenir la présence à partir du serveur pour les contacts auxquels l'application cliente de messagerie instantanée s'est inscrite. La méthode **Subscribe** est utile dans les situations où la présence d'une personne ne figurant pas dans la liste des contacts d'un utilisateur est requise (par exemple, à partir d'un réseau plus grand public).</span><span class="sxs-lookup"><span data-stu-id="30a0d-p155">The **IContactSubscription.Subscribe** method allows an IM client application to access presence observers for the contact. It can use a polling strategy to get the presence from the server for the contacts for that the IM client application has subscribed to. The **Subscribe** method is helpful in situations where presence is requested for someone outside of a user's contact list (for example, from a larger public network).</span></span> 
  
### <a name="icontactendpoint-interface"></a><span data-ttu-id="30a0d-496">Interface IContactEndPoint</span><span class="sxs-lookup"><span data-stu-id="30a0d-496">IContactEndPoint interface</span></span>
<span data-ttu-id="30a0d-497"><a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-497"></span></span>

<span data-ttu-id="30a0d-498">L'interface **IContactEndPoint** représente un numéro de téléphone à partir de la collection de numéros de téléphone d'un contact.</span><span class="sxs-lookup"><span data-stu-id="30a0d-498">The **IContactEndPoint** represents a telephone number from a contact's collection of telephone numbers.</span></span> 
  
<span data-ttu-id="30a0d-499">Le tableau 11 indique les membres qui doivent être implémentés dans les classes qui héritent de **IContactEndPoint**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-499">Table 11 shows the members that must be implemented in the classes that inherit from **IContactEndPoint**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="30a0d-500">Tout membre de l'interface **IContactEndPoint** non répertorié dans le tableau doit être présent, mais ne doit pas nécessairement être implémenté.</span><span class="sxs-lookup"><span data-stu-id="30a0d-500">Any member of the **IContactEndPoint** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="30a0d-501">Les membres présents, mais non implémentés, peuvent générer une erreur**NotImplementedException** ou **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-501">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="30a0d-502">Pour plus d'informations sur l'interface **IContactEndPoint** et ses membres, consultez [UCCollaborationLib.IContactEndpoint](http://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span><span class="sxs-lookup"><span data-stu-id="30a0d-502">> For more information about the **IContactEndPoint** interface and its members, see [UCCollaborationLib.IContactEndpoint](http://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span></span> 
  
<span data-ttu-id="30a0d-503">**Tableau 11. Implémentation de l’interface IContactEndPoint**</span><span class="sxs-lookup"><span data-stu-id="30a0d-503">**Table 11. Implementation of the IContactEndPoint interface**</span></span>

|<span data-ttu-id="30a0d-504">**Membre**</span><span class="sxs-lookup"><span data-stu-id="30a0d-504">**Member**</span></span>|<span data-ttu-id="30a0d-505">**Description**</span><span class="sxs-lookup"><span data-stu-id="30a0d-505">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30a0d-506">Propriété **DisplayName**</span><span class="sxs-lookup"><span data-stu-id="30a0d-506">**DisplayName** property</span></span>  <br/> |<span data-ttu-id="30a0d-507">Obtient la chaîne d’affichage.</span><span class="sxs-lookup"><span data-stu-id="30a0d-507">Gets the display string.</span></span>  <br/> |
|<span data-ttu-id="30a0d-508">Propriété **Type**</span><span class="sxs-lookup"><span data-stu-id="30a0d-508">**Type** property</span></span>  <br/> |<span data-ttu-id="30a0d-509">Obtient le type de point de terminaison du contact.</span><span class="sxs-lookup"><span data-stu-id="30a0d-509">Gets the contact endpoint type</span></span>  <br/> |
|<span data-ttu-id="30a0d-510">Propriété **Uri**</span><span class="sxs-lookup"><span data-stu-id="30a0d-510">**Uri** property</span></span>  <br/> |<span data-ttu-id="30a0d-511">Obtient l’URI du contact.</span><span class="sxs-lookup"><span data-stu-id="30a0d-511">Gets the contact URI.</span></span>  <br/> |
   
### <a name="ilocalestring-interface"></a><span data-ttu-id="30a0d-512">Interface ILocaleString</span><span class="sxs-lookup"><span data-stu-id="30a0d-512">ILocaleString interface</span></span>
<span data-ttu-id="30a0d-513"><a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a></span><span class="sxs-lookup"><span data-stu-id="30a0d-513"></span></span>

<span data-ttu-id="30a0d-p157">L'interface **ILocaleString** est une structure de chaîne localisée contenant une chaîne localisée et l'ID des paramètres régionaux de la localisation. L'interface **ILocaleString** est utilisée pour mettre en forme la chaîne de statut personnalisé sur la carte de visite.</span><span class="sxs-lookup"><span data-stu-id="30a0d-p157">The **ILocaleString** is a localized string structure that contains both a localized string and the locale ID of the localization. The **ILocaleString** interface is used to format the custom status string on the contact card.</span></span> 
  
<span data-ttu-id="30a0d-516">Le tableau 12 affiche les membres qui doivent être implémentés dans les classes qui héritent de **ILocaleString**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-516">Table 12 shows the members that must be implemented in the classes that inherit from **ILocaleString**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="30a0d-517">Tout membre de l'interface **ILocaleString** non répertorié dans le tableau doit être présent, mais ne doit pas nécessairement être implémenté.</span><span class="sxs-lookup"><span data-stu-id="30a0d-517">Any member of the **ILocaleString** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="30a0d-518">Les membres présents, mais non implémentés, peuvent générer une erreur**NotImplementedException** ou **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="30a0d-518">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="30a0d-519">Pour plus d'informations sur l'interface **ILocalString** et ses membres, voir [UCCollaborationLib.ILocaleString](http://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span><span class="sxs-lookup"><span data-stu-id="30a0d-519">> For more information about the **ILocalString** interface and its members, see [UCCollaborationLib.ILocaleString](http://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span></span> 
  
<span data-ttu-id="30a0d-520">**Tableau 12. Implémentation de l’interface ILocaleString**</span><span class="sxs-lookup"><span data-stu-id="30a0d-520">**Table 12. Implementation of the ILocaleString interface**</span></span>

|<span data-ttu-id="30a0d-521">**Membre**</span><span class="sxs-lookup"><span data-stu-id="30a0d-521">**Member**</span></span>|<span data-ttu-id="30a0d-522">**Description**</span><span class="sxs-lookup"><span data-stu-id="30a0d-522">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30a0d-523">Propriété **LocaleId**</span><span class="sxs-lookup"><span data-stu-id="30a0d-523">**LocaleId** property</span></span>  <br/> |<span data-ttu-id="30a0d-524">Obtient l’ID des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="30a0d-524">Gets the locale ID.</span></span>  <br/> |
|<span data-ttu-id="30a0d-525">Propriété **Value**</span><span class="sxs-lookup"><span data-stu-id="30a0d-525">**Value** property</span></span>  <br/> |<span data-ttu-id="30a0d-526">Obtient la chaîne.</span><span class="sxs-lookup"><span data-stu-id="30a0d-526">Gets the string.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30a0d-527">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30a0d-527">See also</span></span>

- <span data-ttu-id="30a0d-528">Espace de noms [UCCollaborationLib](http://msdn.microsoft.com/library/UCCollaborationLib)</span><span class="sxs-lookup"><span data-stu-id="30a0d-528">[UCCollaborationLib](http://msdn.microsoft.com/library/UCCollaborationLib) namespace</span></span> 
    

