---
title: Intégration à Office à partir d'applications iOS
manager: soliver
ms.date: 06/04/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f3a277ba-7ba1-4eea-83b5-915b409f3093
description: Office pour iOS fournit une solution extensible qui permet l'intégration à des applications tierces. Cet article explique comment effectuer une intégration à Office à partir de votre application iOS en transférant les utilisateurs de votre application vers Office, puis en les renvoyant vers votre application.
ms.openlocfilehash: 66106c51706a9ab1cd0e36b51340e65ccb807902
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595327"
---
# <a name="integrate-with-office-from-ios-applications"></a><span data-ttu-id="5acab-104">Intégration à Office à partir d'applications iOS</span><span class="sxs-lookup"><span data-stu-id="5acab-104">Integrate with Office from iOS applications</span></span>

<span data-ttu-id="5acab-p102">Office pour iOS fournit une solution extensible qui permet l'intégration à des applications tierces. Cet article explique comment effectuer une intégration à Office à partir de votre application iOS en transférant les utilisateurs de votre application vers Office, puis en les renvoyant vers votre application.</span><span class="sxs-lookup"><span data-stu-id="5acab-p102">Office for iOS provides an extensible solution that enables integration with third-party applications. This article describes how you can integrate with Office from your iOS application by passing users from your application to Office, and then returning them to your application.</span></span>
  
<span data-ttu-id="5acab-p103">Vous pouvez permettre aux utilisateurs exécutant Office sur un périphérique iOS d'ouvrir et de modifier des fichiers stockés dans SharePoint ou OneDrive à partir de n'importe quelle application, puis les renvoyer rapidement vers l'application d'origine lorsqu'ils ont terminé la modification du fichier. Pour ce faire, vous transférez les fichiers à Office via des gestionnaires de protocole et vous vous assurez qu'Office est appelé d'une manière qu'Office peut comprendre.</span><span class="sxs-lookup"><span data-stu-id="5acab-p103">You can enable users who are running Office on an iOS device to open and edit files stored in SharePoint or OneDrive from any application, and then quickly return them to the original application when they're done editing the file. To do this, you pass files to Office via protocol handlers, and you make sure that Office is invoked in a way that Office can understand.</span></span>
  
<span data-ttu-id="5acab-109">Lorsqu'un utilisateur a terminé la modification d'un fichier, il peut sélectionner la flèche de retour dans l'application Office pour fermer le document et revenir à l'application de stockage d'origine, pour autant que vous transmettiez des informations spécifiques à l'application Office à son lancement.</span><span class="sxs-lookup"><span data-stu-id="5acab-109">When a user is done editing a file, they can choose the back arrow in the Office application to close the document and return to the original storage application, provided you pass specific information to the Office application when it launches.</span></span>
  
## <a name="verify-that-office-has-been-installed"></a><span data-ttu-id="5acab-110">Vérifier qu'Office a été installé</span><span class="sxs-lookup"><span data-stu-id="5acab-110">Verify that Office has been installed</span></span>

<span data-ttu-id="5acab-p104">Votre application référente doit d'abord vérifier qu'une application Office particulière est installée. Les applications Office suivantes peuvent être installées sur des périphériques iOS pour l'affichage et la modification de documents :</span><span class="sxs-lookup"><span data-stu-id="5acab-p104">Your referring application will first need to verify that a particular Office application is installed. The following Office applications can be installed on iOS devices for document viewing and editing:</span></span>
  
- <span data-ttu-id="5acab-113">Excel</span><span class="sxs-lookup"><span data-stu-id="5acab-113">Excel</span></span>
    
- <span data-ttu-id="5acab-114">OneNote</span><span class="sxs-lookup"><span data-stu-id="5acab-114">OneNote</span></span>
    
- <span data-ttu-id="5acab-115">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="5acab-115">PowerPoint</span></span>
    
- <span data-ttu-id="5acab-116">Word</span><span class="sxs-lookup"><span data-stu-id="5acab-116">Word</span></span>
    
<span data-ttu-id="5acab-p105">Utilisez la méthode [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) pour déterminer si votre application peut ouvrir la ressource. Cette méthode prend l'URL de la ressource comme paramètre, puis renvoie **No** si l'application qui accepte l'URL n'est pas disponible. Si **canOpenURL** renvoie **No**, vous devez inviter l'utilisateur à installer Office.</span><span class="sxs-lookup"><span data-stu-id="5acab-p105">Use the [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) method to determine whether your application can open the resource. This method takes the URL for the resource as a parameter, and returns **No** if the application that accepts the URL is not available. If **canOpenURL** returns **No**, you'll need to prompt the user to install Office.</span></span>
  
### <a name="prompt-the-user-to-install-office"></a><span data-ttu-id="5acab-120">Inviter l'utilisateur à installer Office</span><span class="sxs-lookup"><span data-stu-id="5acab-120">Prompt the user to install Office</span></span>

 <span data-ttu-id="5acab-p106">Si une application Office particulière n'est pas installée, vous pouvez utiliser un objet [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) pour afficher l'App Store iTunes dans votre application et montrer à l'utilisateur l'application Office à installer. Le tableau suivant indique l'identifiant iTunes à utiliser pour appeler chaque application Office dans Store Kit Product View Controller.</span><span class="sxs-lookup"><span data-stu-id="5acab-p106">If a particular Office application is not installed, you can use an [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) object to render the iTunes app store in your application and show the user the Office application to install. The following table lists the iTunes identifier to use to invoke each Office application in the Store Kit Product View Controller.</span></span> 
  
|<span data-ttu-id="5acab-123">**Application Office**</span><span class="sxs-lookup"><span data-stu-id="5acab-123">**Office application**</span></span>|<span data-ttu-id="5acab-124">**Identifiant iTunes**</span><span class="sxs-lookup"><span data-stu-id="5acab-124">**iTunes identifier**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5acab-125">Excel</span><span class="sxs-lookup"><span data-stu-id="5acab-125">Excel</span></span>  <br/> |[<span data-ttu-id="5acab-126">https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="5acab-126">https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="5acab-127">OneNote (iPhone)</span><span class="sxs-lookup"><span data-stu-id="5acab-127">OneNote (iPhone)</span></span>  <br/> |[<span data-ttu-id="5acab-128">https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="5acab-128">https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="5acab-129">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="5acab-129">PowerPoint</span></span>  <br/> |[<span data-ttu-id="5acab-130">https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="5acab-130">https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="5acab-131">Word</span><span class="sxs-lookup"><span data-stu-id="5acab-131">Word</span></span>  <br/> |[<span data-ttu-id="5acab-132">https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="5acab-132">https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4) <br/> |
   
## <a name="invoke-office"></a><span data-ttu-id="5acab-133">Appeler Office</span><span class="sxs-lookup"><span data-stu-id="5acab-133">Invoke Office</span></span>

<span data-ttu-id="5acab-134">Lorsque l'application Office est installée, votre application référente peut appeler Office en transmettant les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="5acab-134">When the Office application is installed, your referring application can invoke Office by passing the following details:</span></span> 
  
- <span data-ttu-id="5acab-135">Protocole Office</span><span class="sxs-lookup"><span data-stu-id="5acab-135">Office protocol</span></span>
    
- <span data-ttu-id="5acab-136">Mode d'ouverture</span><span class="sxs-lookup"><span data-stu-id="5acab-136">Open mode</span></span>
    
- <span data-ttu-id="5acab-137">URL</span><span class="sxs-lookup"><span data-stu-id="5acab-137">URL</span></span>
    
- <span data-ttu-id="5acab-138">Protocole de transmission retour</span><span class="sxs-lookup"><span data-stu-id="5acab-138">Passback protocol</span></span>
    
- <span data-ttu-id="5acab-139">Contexte de document</span><span class="sxs-lookup"><span data-stu-id="5acab-139">Document context</span></span>
    
<span data-ttu-id="5acab-140">Format de schéma :</span><span class="sxs-lookup"><span data-stu-id="5acab-140">Schema format:</span></span>
  
 `<Office protocol><open mode>|u|<URL>|p|<passback protocol>|c|<document context>`
  
<span data-ttu-id="5acab-141">L'exemple suivant montre une demande d'appel de fichier Word pour modification :</span><span class="sxs-lookup"><span data-stu-id="5acab-141">The following example shows a request to invoke a Word file for editing:</span></span>
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx|p|clouddrive|c|folderviewQ4`
  
### <a name="office-protocols"></a><span data-ttu-id="5acab-142">Protocoles Office</span><span class="sxs-lookup"><span data-stu-id="5acab-142">Office protocols</span></span>

<span data-ttu-id="5acab-143">Le tableau suivant répertorie les protocoles pour chaque application Office.</span><span class="sxs-lookup"><span data-stu-id="5acab-143">The following table lists the protocols for each Office application.</span></span> 
  
|<span data-ttu-id="5acab-144">**Application**</span><span class="sxs-lookup"><span data-stu-id="5acab-144">**Application**</span></span>|<span data-ttu-id="5acab-145">**Protocole**</span><span class="sxs-lookup"><span data-stu-id="5acab-145">**Protocol**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5acab-146">Excel</span><span class="sxs-lookup"><span data-stu-id="5acab-146">Excel</span></span>  <br/> |<span data-ttu-id="5acab-147">ms-excel:</span><span class="sxs-lookup"><span data-stu-id="5acab-147">ms-excel:</span></span>  <br/> |
|<span data-ttu-id="5acab-148">OneNote</span><span class="sxs-lookup"><span data-stu-id="5acab-148">OneNote</span></span>  <br/> |<span data-ttu-id="5acab-149">onenote:</span><span class="sxs-lookup"><span data-stu-id="5acab-149">onenote:</span></span>  <br/> |
|<span data-ttu-id="5acab-150">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="5acab-150">PowerPoint</span></span>  <br/> |<span data-ttu-id="5acab-151">ms-powerpoint:</span><span class="sxs-lookup"><span data-stu-id="5acab-151">ms-powerpoint:</span></span>  <br/> |
|<span data-ttu-id="5acab-152">Word</span><span class="sxs-lookup"><span data-stu-id="5acab-152">Word</span></span>  <br/> |<span data-ttu-id="5acab-153">ms-word:</span><span class="sxs-lookup"><span data-stu-id="5acab-153">ms-word:</span></span>  <br/> |
   
### <a name="open-mode"></a><span data-ttu-id="5acab-154">Mode d'ouverture</span><span class="sxs-lookup"><span data-stu-id="5acab-154">Open mode</span></span>

<span data-ttu-id="5acab-p107">Les applications Office peuvent ouvrir les fichiers directement en mode d'affichage (ofv) ou de modification (ofe), ce dernier étant le mode par défaut.</span><span class="sxs-lookup"><span data-stu-id="5acab-p107">Office applications can open files directly into view (ofv) or edit (ofe) mode. Edit mode is the default.</span></span> 
  
<span data-ttu-id="5acab-157">Format de schéma :</span><span class="sxs-lookup"><span data-stu-id="5acab-157">Schema format:</span></span>
  
 `<ofv or ofe>`
  
### <a name="url"></a><span data-ttu-id="5acab-158">URL</span><span class="sxs-lookup"><span data-stu-id="5acab-158">URL</span></span>

<span data-ttu-id="5acab-159">L'URL comprend trois parties :</span><span class="sxs-lookup"><span data-stu-id="5acab-159">The URL includes three parts:</span></span> 
  
- <span data-ttu-id="5acab-160">Déclaration indiquant que le fichier est ouvert pour modification (ofe)</span><span class="sxs-lookup"><span data-stu-id="5acab-160">The declaration that the file will be opened for edit (ofe)</span></span>
    
- <span data-ttu-id="5acab-161">Descripteur de l'URL (|u|)</span><span class="sxs-lookup"><span data-stu-id="5acab-161">The URL descriptor (|u|)</span></span>
    
- <span data-ttu-id="5acab-162">URL</span><span class="sxs-lookup"><span data-stu-id="5acab-162">The URL</span></span>
    
<span data-ttu-id="5acab-p108">L'URL doit être codée et il doit s'agir d'un lien direct vers le fichier (et non d'une redirection). Si le format de l'URL ne peut pas être géré par Office ou en cas d'échec du téléchargement, Office ne renvoie pas l'utilisateur vers l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="5acab-p108">The URL has to be encoded and must be a direct link to the file (not a redirect). If the URL is in a format that Office cannot handle, or the download simply fails, Office will not return the user to the invoking application.</span></span> 
  
<span data-ttu-id="5acab-165">Format de schéma :</span><span class="sxs-lookup"><span data-stu-id="5acab-165">Schema format:</span></span>
  
 `|u|<document URL>`
  
### <a name="passback-protocol-optional"></a><span data-ttu-id="5acab-166">Protocole de transmission retour (facultatif)</span><span class="sxs-lookup"><span data-stu-id="5acab-166">Passback protocol (optional)</span></span>

<span data-ttu-id="5acab-p109">Si vous voulez qu'Office renvoie les utilisateurs vers votre application iOS lorsqu'ils choisissent la flèche de retour, l'application appelante doit utiliser le protocole de transmission retour, qui comprend le descripteur « |p| » suivi du protocole de l'application (sans signe deux-points). Assurez-vous que votre application peut gérer correctement la réponse d'Office.</span><span class="sxs-lookup"><span data-stu-id="5acab-p109">If you want Office to return users to your iOS application when they choose the back arrow, the invoking application will need to use the passback protocol, which includes the descriptor '|p|' followed by the app protocol (without a colon). You'll need to ensure that your application can properly handle the response from Office.</span></span>
  
<span data-ttu-id="5acab-169">Format de schéma :</span><span class="sxs-lookup"><span data-stu-id="5acab-169">Schema format:</span></span>
  
 `|p|<passback protocol>`
  
### <a name="document-context-optional"></a><span data-ttu-id="5acab-170">Contexte de document (facultatif)</span><span class="sxs-lookup"><span data-stu-id="5acab-170">Document context (optional)</span></span>

<span data-ttu-id="5acab-p110">Office n'utilise pas le contexte du document, mais l'application référente peut en avoir besoin lorsque Office transmet un utilisateur en retour. Si vous voulez que le contexte de document soit renvoyé vers votre application, utilisez le descripteur « |c| » suivi du contexte que vous voulez comme chaîne. Office ne limite pas la longueur de la chaîne, au-delà des limites imposées par le système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="5acab-p110">Office doesn't use the document context, but the referring application might need it when Office passes a user back. If you want the document context to be returned to your application, use the descriptor '|c|' followed by the context that you want as a string. Office does not limit the length of the string, beyond any limits imposed by the operating system.</span></span>
  
<span data-ttu-id="5acab-174">Format de schéma :</span><span class="sxs-lookup"><span data-stu-id="5acab-174">Schema format:</span></span>
  
 `|c|<document context>`
  
## <a name="return-users-to-the-referring-application"></a><span data-ttu-id="5acab-175">Renvoyer les utilisateurs vers l'application référente</span><span class="sxs-lookup"><span data-stu-id="5acab-175">Return users to the referring application</span></span>

<span data-ttu-id="5acab-p111">Pour des raisons de sécurité, Office renvoie uniquement les utilisateurs vers l'application référente si le fichier a été ouvert. Lorsque l'utilisateur sélectionne la flèche de retour, Office répond à l'application appelante avec le protocole de transmission retour, le mode d'ouverture, l'URL, l'état de téléchargement en attente et le contexte de document. L'état de téléchargement en attente utilise le descripteur |z| et prend la valeur Oui ou Non.</span><span class="sxs-lookup"><span data-stu-id="5acab-p111">For security reasons, Office only returns users to the referring application if the file opened successfully. When the user chooses the back arrow, Office responds to the invoking application with the passback protocol, open mode, URL, upload pending status, and document context. The upload pending status uses the descriptor |z|, and is either yes or no.</span></span>
  
<span data-ttu-id="5acab-179">Format de schéma :</span><span class="sxs-lookup"><span data-stu-id="5acab-179">Schema format:</span></span>
  
 `<app protocol>:ofe|u|<URL>|z|<yes or no>|c|<doc context> Example: clouddrive:ofe|u|https://contoso/Q4/budget.docx|z|no|c|folderviewQ4`
  
## <a name="see-also"></a><span data-ttu-id="5acab-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5acab-180">See also</span></span>
<span data-ttu-id="5acab-181"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="5acab-181"></span></span>

- [<span data-ttu-id="5acab-182">Méthode canOpenURL</span><span class="sxs-lookup"><span data-stu-id="5acab-182">canOpenURL method</span></span>](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [<span data-ttu-id="5acab-183">Classe UIApplication</span><span class="sxs-lookup"><span data-stu-id="5acab-183">UIApplication class</span></span>](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [<span data-ttu-id="5acab-184">Objet SKProductViewController</span><span class="sxs-lookup"><span data-stu-id="5acab-184">SKProductViewController object</span></span>](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)
    

