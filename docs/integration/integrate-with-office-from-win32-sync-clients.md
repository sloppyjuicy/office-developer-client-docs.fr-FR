---
title: Intégration à Office à partir de clients de synchronisation Win32
manager: soliver
ms.date: 07/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 348555d3-3cd4-4e4a-b5ad-436571c25251
description: Intégrez vos clients de synchronisation Win32 tiers à des applications Office Excel Mobile, PowerPoint Mobile et Word Mobile.
ms.openlocfilehash: 9f520ad36583a9aa7cd73638fe92158f70d13daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782481"
---
# <a name="integrate-with-office-from-win32-sync-clients"></a><span data-ttu-id="7aa6b-103">Intégration à Office à partir de clients de synchronisation Win32</span><span class="sxs-lookup"><span data-stu-id="7aa6b-103">Integrate with Office from Win32 sync clients</span></span>

<span data-ttu-id="7aa6b-104">Intégrez vos clients de synchronisation Win32 tiers à des applications Office Excel Mobile, PowerPoint Mobile et Word Mobile.</span><span class="sxs-lookup"><span data-stu-id="7aa6b-104">Integrate your third-party Win32 sync clients with Excel Mobile, PowerPoint Mobile, and Word Mobile Office applications.</span></span> 
  
<span data-ttu-id="7aa6b-p101">Vous pouvez intégrer votre application universelle Windows à des clients Excel Mobile, PowerPoint Mobile et Word Mobile en vous inscrivant en tant que fournisseur racine de synchronisation. Cet article décrit les meilleures pratiques à appliquer pour vous assurer que vos clients de synchronisation Win32 fonctionnent correctement avec les applications Office.</span><span class="sxs-lookup"><span data-stu-id="7aa6b-p101">You can integrate your Windows universal app with Excel Mobile, PowerPoint Mobile, and Word Mobile clients by registering as a sync root provider. This article describes the best practices to apply to ensure that your Win32 sync clients work well with Office applications.</span></span>
  
<span data-ttu-id="7aa6b-107">Cette intégration exige que votre client de synchronisation Win32 dispose d'un moteur de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="7aa6b-107">This integration requires that your Win32 sync client has a sync engine.</span></span>
  
## <a name="register-as-a-sync-root-provider"></a><span data-ttu-id="7aa6b-108">Inscription en tant que fournisseur racine de synchronisation</span><span class="sxs-lookup"><span data-stu-id="7aa6b-108">Register as a sync root provider</span></span>

<span data-ttu-id="7aa6b-p102">Sauf dans le cas où votre client de synchronisation est inscrit en tant que fournisseur racine de synchronisation, Office traite les fichiers de votre dossier de synchronisation de la manière dont il traite les fichiers locaux standard. Cela signifie qu'Office fournit des options de déplacement vers OneDrive pour les utilisateurs lorsqu'ils tentent de partager le document. Afin d'éviter ce problème pour les fichiers que vous synchronisez, vous devez vous inscrire en tant que fournisseur racine de synchronisation. Pour plus d'informations sur l'inscription, voir [Intégration d'un fournisseur de stockage cloud](https://msdn.microsoft.com/fr-FR/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7aa6b-p102">Unless your sync client is registered as a sync root provider, Office will treat files in your sync folder the way that it treats regular local files. This means that Office will provide "move to OneDrive" options for users when they attempt to share the document. To avoid this for files you sync, you must register as a sync root provider. For information about how to register, see [Integrate a Cloud Storage Provider](https://msdn.microsoft.com/fr-FR/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span></span>
  
## <a name="integrate-your-app-into-the-root-node-of-the-navigation-pane"></a><span data-ttu-id="7aa6b-113">Intégration de votre application dans le nœud racine du volet de navigation</span><span class="sxs-lookup"><span data-stu-id="7aa6b-113">Integrate your app into the root node of the navigation pane</span></span>

<span data-ttu-id="7aa6b-p103">Afin que votre client de synchronisation Win32 apparaisse sous la forme d'un nœud racine au sein du volet de navigation dans l'Explorateur de fichiers et le sélecteur de fichiers Windows, vous devez intégrer votre application au niveau racine. Pour plus d'informations sur la procédure à suivre, voir [Intégration d'un fournisseur de stockage cloud](https://msdn.microsoft.com/fr-FR/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7aa6b-p103">In order for your Win32 sync client to show up as a root node in the navigation pane in the File Explorer and Windows file picker, you need to integrate your app into the root level. For information about how to do this, see [Integrate a Cloud Storage Provider](https://msdn.microsoft.com/fr-FR/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span></span> 
  
## <a name="add-your-sync-folder-as-a-document-library-optional"></a><span data-ttu-id="7aa6b-116">Ajout de votre dossier de synchronisation en tant que bibliothèque de documents (facultatif)</span><span class="sxs-lookup"><span data-stu-id="7aa6b-116">Add your sync folder as a document library (optional)</span></span>

<span data-ttu-id="7aa6b-p104">Dans Office, les utilisateurs peuvent créer des documents dans leurs bibliothèques de documents à l'aide d'une seule action. Pour ajouter votre emplacement de synchronisation à la bibliothèque de documents, utilisez la fonction [SHAddFolderPathToLibrary](https://msdn.microsoft.com/fr-FR/library/windows/desktop/dd378432%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7aa6b-p104">In Office, users can create documents in their document libraries with a single action. To add your sync location to the document library, use the [SHAddFolderPathToLibrary function](https://msdn.microsoft.com/fr-FR/library/windows/desktop/dd378432%28v=vs.85%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7aa6b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7aa6b-119">See also</span></span>
<span data-ttu-id="7aa6b-120"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="7aa6b-120"></span></span>

- [<span data-ttu-id="7aa6b-121">Intégration à Office</span><span class="sxs-lookup"><span data-stu-id="7aa6b-121">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="7aa6b-122">Intégration à Office à partir d'applications universelles Windows</span><span class="sxs-lookup"><span data-stu-id="7aa6b-122">Integrate with Office from Windows universal apps</span></span>](integrate-with-office-from-windows-universal-apps.md)
    

