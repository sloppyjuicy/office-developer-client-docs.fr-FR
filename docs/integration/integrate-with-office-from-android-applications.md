---
title: Intégration à Office à partir d'applications Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a765fa49-a272-4047-9147-59cc68e5dd27
description: Office pour Android fournit une solution extensible qui permet l'intégration avec des applications tierces. Vous pouvez exécuter une intégration avec Office à partir de votre application Android en transférant les utilisateurs de votre application vers Office.
ms.openlocfilehash: 4e674b3d66f3acba7e9c9c19e716ff0d73d803b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303149"
---
# <a name="integrate-with-office-from-android-applications"></a><span data-ttu-id="b9c98-104">Intégration à Office à partir d'applications Android</span><span class="sxs-lookup"><span data-stu-id="b9c98-104">Integrate with Office from Android applications</span></span>

<span data-ttu-id="b9c98-p102">Office pour Android fournit une solution extensible qui permet l'intégration avec des applications tierces. Vous pouvez exécuter une intégration avec Office à partir de votre application Android en transférant les utilisateurs de votre application vers Office.</span><span class="sxs-lookup"><span data-stu-id="b9c98-p102">Office for Android provides an extensible solution that enables integration with third-party applications. You can integrate with Office from your Android application by passing users from your application to Office.</span></span>
  
<span data-ttu-id="b9c98-p103">Vous pouvez permettre aux utilisateurs qui exécutent Office sur un appareil Android d'ouvrir et de modifier les fichiers stockés dans SharePoint ou OneDrive à partir de n'importe quelle application. Pour ce faire, transférez les fichiers vers Office par l'intermédiaire de gestionnaires de protocole et assurez-vous qu'Office est invoqué de manière à ce qu'Office puisse comprendre.</span><span class="sxs-lookup"><span data-stu-id="b9c98-p103">You can enable users who are running Office on an Android device to open and edit files stored in SharePoint or OneDrive from any application. To do this, you pass files to Office via protocol handlers, and you make sure that Office is invoked in a way that Office can understand.</span></span>
  
<span data-ttu-id="b9c98-109">Une fois le fichier édité par l'utilisateur, ce dernier peut appuyer sur la touche de retour de l'appareil pour revenir à l'application de stockage d'origine.</span><span class="sxs-lookup"><span data-stu-id="b9c98-109">When a user is done editing a file, they can choose the back key on the device to return to the original storage application.</span></span>
  
## <a name="verify-that-office-has-been-installed"></a><span data-ttu-id="b9c98-110">Assurez-vous qu'Office est bien installé</span><span class="sxs-lookup"><span data-stu-id="b9c98-110">Verify that Office has been installed</span></span>

<span data-ttu-id="b9c98-p104">Votre application référente doit d'abord vérifier qu'une application Office particulière est installée. Les applications Office suivantes peuvent être installées sur des périphériques Android pour l'affichage et la modification de documents :</span><span class="sxs-lookup"><span data-stu-id="b9c98-p104">Your referring application will first need to verify that a particular Office application is installed. The following Office applications can be installed on Android devices for document viewing and editing:</span></span> 
  
- <span data-ttu-id="b9c98-113">Excel</span><span class="sxs-lookup"><span data-stu-id="b9c98-113">Excel</span></span>
    
- <span data-ttu-id="b9c98-114">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="b9c98-114">PowerPoint</span></span>
    
- <span data-ttu-id="b9c98-115">Word</span><span class="sxs-lookup"><span data-stu-id="b9c98-115">Word</span></span>
    
<span data-ttu-id="b9c98-p105">Utilisez Android PackageManager pour déterminer si une application Office spécifique est installée sur l'appareil. Le tableau suivant répertorie les noms des paquets pour les applications Office que vous pouvez utiliser dans ce processus.</span><span class="sxs-lookup"><span data-stu-id="b9c98-p105">Use Android PackageManager to determine whether a particular Office application is installed on the device. The following table lists the package names for the Office applications that you can use in this process.</span></span>
  
|<span data-ttu-id="b9c98-118">**Application**</span><span class="sxs-lookup"><span data-stu-id="b9c98-118">**Application**</span></span>|<span data-ttu-id="b9c98-119">**Nom du paquet**</span><span class="sxs-lookup"><span data-stu-id="b9c98-119">**Package name**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9c98-120">Excel</span><span class="sxs-lookup"><span data-stu-id="b9c98-120">Excel</span></span>  <br/> |<span data-ttu-id="b9c98-121">com.microsoft.office.excel</span><span class="sxs-lookup"><span data-stu-id="b9c98-121">com.microsoft.office.excel</span></span>  <br/> |
|<span data-ttu-id="b9c98-122">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="b9c98-122">PowerPoint</span></span>  <br/> |<span data-ttu-id="b9c98-123">com.microsoft.office.powerpoint</span><span class="sxs-lookup"><span data-stu-id="b9c98-123">com.microsoft.office.powerpoint</span></span>  <br/> |
|<span data-ttu-id="b9c98-124">Word</span><span class="sxs-lookup"><span data-stu-id="b9c98-124">Word</span></span>  <br/> |<span data-ttu-id="b9c98-125">com.microsoft.office.word</span><span class="sxs-lookup"><span data-stu-id="b9c98-125">com.microsoft.office.word</span></span>  <br/> |
   
### <a name="prompt-the-user-to-install-office"></a><span data-ttu-id="b9c98-126">Inviter l'utilisateur à installer Office</span><span class="sxs-lookup"><span data-stu-id="b9c98-126">Prompt the user to install Office</span></span>

<span data-ttu-id="b9c98-p106">Si une application Office spécifique n'est pas installée, vous pouvez inviter l'utilisateur à l'installer. Le tableau suivant répertorie les emplacements d'installation disponibles pour les applications Office.</span><span class="sxs-lookup"><span data-stu-id="b9c98-p106">If a particular Office application is not installed, you can prompt the user to install the application. The following table lists the available install locations for Office applications.</span></span>
  
|<span data-ttu-id="b9c98-129">**Application**</span><span class="sxs-lookup"><span data-stu-id="b9c98-129">**Application**</span></span>|<span data-ttu-id="b9c98-130">**Google Play Store**</span><span class="sxs-lookup"><span data-stu-id="b9c98-130">**Google Play Store**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9c98-131">Excel</span><span class="sxs-lookup"><span data-stu-id="b9c98-131">Excel</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.excel](https://play.google.com/store/apps/details?id=com.microsoft.office.excel) <br/> |
|<span data-ttu-id="b9c98-132">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="b9c98-132">PowerPoint</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint](https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint) <br/> |
|<span data-ttu-id="b9c98-133">Word</span><span class="sxs-lookup"><span data-stu-id="b9c98-133">Word</span></span>  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.word](https://play.google.com/store/apps/details?id=com.microsoft.office.word) <br/> |
   
## <a name="invoke-office"></a><span data-ttu-id="b9c98-134">Appeler Office</span><span class="sxs-lookup"><span data-stu-id="b9c98-134">Invoke Office</span></span>

<span data-ttu-id="b9c98-135">Lorsque l'application Office est installée, votre application référente peut appeler Office en transmettant les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b9c98-135">When the Office application is installed, your referring application can invoke Office by passing the following details:</span></span>
  
- <span data-ttu-id="b9c98-136">Protocole Office</span><span class="sxs-lookup"><span data-stu-id="b9c98-136">Office protocol</span></span>
    
- <span data-ttu-id="b9c98-137">Mode d'ouverture</span><span class="sxs-lookup"><span data-stu-id="b9c98-137">Open mode</span></span>
    
- <span data-ttu-id="b9c98-138">URL</span><span class="sxs-lookup"><span data-stu-id="b9c98-138">URL</span></span>
    
<span data-ttu-id="b9c98-139">Format de schéma :</span><span class="sxs-lookup"><span data-stu-id="b9c98-139">Schema format:</span></span>
  
 `<Office protocol><open mode>|u|<URL>`
  
<span data-ttu-id="b9c98-140">L'exemple suivant montre une demande d'appel de fichier Word pour modification :</span><span class="sxs-lookup"><span data-stu-id="b9c98-140">The following example shows a request to invoke a Word file for editing.</span></span>
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx`
  
### <a name="office-protocols"></a><span data-ttu-id="b9c98-141">Protocoles Office</span><span class="sxs-lookup"><span data-stu-id="b9c98-141">Office protocols</span></span>

<span data-ttu-id="b9c98-142">Le tableau suivant répertorie les protocoles pour chaque application Office.</span><span class="sxs-lookup"><span data-stu-id="b9c98-142">The following table lists the protocols for each Office application.</span></span>
  
|<span data-ttu-id="b9c98-143">**Application**</span><span class="sxs-lookup"><span data-stu-id="b9c98-143">**Application**</span></span>|<span data-ttu-id="b9c98-144">**Protocole**</span><span class="sxs-lookup"><span data-stu-id="b9c98-144">**Protocol**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9c98-145">Excel</span><span class="sxs-lookup"><span data-stu-id="b9c98-145">Excel</span></span>  <br/> |<span data-ttu-id="b9c98-146">ms-excel:</span><span class="sxs-lookup"><span data-stu-id="b9c98-146">ms-excel:</span></span>  <br/> |
|<span data-ttu-id="b9c98-147">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="b9c98-147">PowerPoint</span></span>  <br/> |<span data-ttu-id="b9c98-148">ms-powerpoint:</span><span class="sxs-lookup"><span data-stu-id="b9c98-148">ms-powerpoint:</span></span>  <br/> |
|<span data-ttu-id="b9c98-149">Word</span><span class="sxs-lookup"><span data-stu-id="b9c98-149">Word</span></span>  <br/> |<span data-ttu-id="b9c98-150">ms-word:</span><span class="sxs-lookup"><span data-stu-id="b9c98-150">ms-word:</span></span>  <br/> |
   
### <a name="open-mode"></a><span data-ttu-id="b9c98-151">Mode d'ouverture</span><span class="sxs-lookup"><span data-stu-id="b9c98-151">Open mode</span></span>

<span data-ttu-id="b9c98-p107">Les applications Office peuvent ouvrir les fichiers directement en mode d'affichage (ofv) ou de modification (ofe), ce dernier étant le mode par défaut.</span><span class="sxs-lookup"><span data-stu-id="b9c98-p107">Office applications can open files directly into view (ofv) or edit (ofe) mode. Edit mode is the default.</span></span>
  
<span data-ttu-id="b9c98-154">Format de schéma :</span><span class="sxs-lookup"><span data-stu-id="b9c98-154">Schema format:</span></span>
  
 `<ofv or ofe>`
  
### <a name="url"></a><span data-ttu-id="b9c98-155">URL</span><span class="sxs-lookup"><span data-stu-id="b9c98-155">URL</span></span>

<span data-ttu-id="b9c98-156">L'URL comprend trois parties :</span><span class="sxs-lookup"><span data-stu-id="b9c98-156">The URL includes three parts:</span></span>
  
- <span data-ttu-id="b9c98-157">Déclaration indiquant que le fichier est ouvert pour modification (ofe)</span><span class="sxs-lookup"><span data-stu-id="b9c98-157">The declaration that the file will be opened for edit (ofe)</span></span>
    
- <span data-ttu-id="b9c98-158">Descripteur de l'URL (|u|)</span><span class="sxs-lookup"><span data-stu-id="b9c98-158">The URL descriptor (|u|)</span></span>
    
- <span data-ttu-id="b9c98-159">URL</span><span class="sxs-lookup"><span data-stu-id="b9c98-159">The URL</span></span>
    
<span data-ttu-id="b9c98-p108">L'URL doit être codée et il doit s'agir d'un lien direct vers le fichier (et non d'une redirection). Si le format de l'URL ne peut pas être géré par Office ou en cas d'échec du téléchargement, Office ne renvoie pas l'utilisateur vers l'application appelante.</span><span class="sxs-lookup"><span data-stu-id="b9c98-p108">The URL has to be encoded and must be a direct link to the file (not a redirect). If the URL is in a format that Office cannot handle, or the download simply fails, Office will not return the user to the invoking application.</span></span>
  
<span data-ttu-id="b9c98-162">Format de schéma :</span><span class="sxs-lookup"><span data-stu-id="b9c98-162">Schema format:</span></span>
  
 `|u|<document URL>`
  
## <a name="see-also"></a><span data-ttu-id="b9c98-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9c98-163">See also</span></span>
<span data-ttu-id="b9c98-164"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="b9c98-164"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="b9c98-165">Intégration à Office</span><span class="sxs-lookup"><span data-stu-id="b9c98-165">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="b9c98-166">PackageManager</span><span class="sxs-lookup"><span data-stu-id="b9c98-166">PackageManager</span></span>](https://developer.android.com/reference/android/content/pm/PackageManager.html)
    
- [<span data-ttu-id="b9c98-167">GetPackageManager()</span><span class="sxs-lookup"><span data-stu-id="b9c98-167">GetPackageManager()</span></span>](https://developer.android.com/reference/android/content/Context.html)
    

