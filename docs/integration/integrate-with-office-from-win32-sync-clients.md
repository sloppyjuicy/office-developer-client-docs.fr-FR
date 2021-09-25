---
title: Intégration à Office à partir de clients de synchronisation Win32
manager: soliver
ms.date: 07/29/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 348555d3-3cd4-4e4a-b5ad-436571c25251
description: Intégrez vos clients de synchronisation Win32 tiers à des applications Office Excel Mobile, PowerPoint Mobile et Word Mobile.
ms.openlocfilehash: ad0c93bb03ba3b23c8395853bec77b8dec29a333
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557336"
---
# <a name="integrate-with-office-from-win32-sync-clients"></a>Intégration à Office à partir de clients de synchronisation Win32

Intégrez vos clients de synchronisation Win32 tiers à des applications Office Excel Mobile, PowerPoint Mobile et Word Mobile. 
  
Vous pouvez intégrer votre application universelle Windows à des clients Excel Mobile, PowerPoint Mobile et Word Mobile en vous inscrivant en tant que fournisseur racine de synchronisation. Cet article décrit les meilleures pratiques à appliquer pour vous assurer que vos clients de synchronisation Win32 fonctionnent correctement avec les applications Office.
  
Cette intégration exige que votre client de synchronisation Win32 dispose d'un moteur de synchronisation.
  
## <a name="register-as-a-sync-root-provider"></a>Inscription en tant que fournisseur racine de synchronisation

Sauf dans le cas où votre client de synchronisation est inscrit en tant que fournisseur racine de synchronisation, Office traite les fichiers de votre dossier de synchronisation de la manière dont il traite les fichiers locaux standard. Cela signifie qu'Office fournit des options de déplacement vers OneDrive pour les utilisateurs lorsqu'ils tentent de partager le document. Afin d'éviter ce problème pour les fichiers que vous synchronisez, vous devez vous inscrire en tant que fournisseur racine de synchronisation. Pour plus d'informations sur l'inscription, voir [Intégration d'un fournisseur de stockage cloud](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).
  
## <a name="integrate-your-app-into-the-root-node-of-the-navigation-pane"></a>Intégration de votre application dans le nœud racine du volet de navigation

Afin que votre client de synchronisation Win32 apparaisse sous la forme d'un nœud racine au sein du volet de navigation dans l'Explorateur de fichiers et le sélecteur de fichiers Windows, vous devez intégrer votre application au niveau racine. Pour plus d'informations sur la procédure à suivre, voir [Intégration d'un fournisseur de stockage cloud](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx). 
  
## <a name="add-your-sync-folder-as-a-document-library-optional"></a>Ajout de votre dossier de synchronisation en tant que bibliothèque de documents (facultatif)

Dans Office, les utilisateurs peuvent créer des documents dans leurs bibliothèques de documents à l'aide d'une seule action. Pour ajouter votre emplacement de synchronisation à la bibliothèque de documents, utilisez la fonction [SHAddFolderPathToLibrary](https://msdn.microsoft.com/library/windows/desktop/dd378432%28v=vs.85%29.aspx). 
  
## <a name="see-also"></a>Voir aussi
<a name="bk_addresources"> </a>

- [Intégration à Office](integrate-with-office.md)
    
- [Intégration à Office à partir d'applications universelles Windows](integrate-with-office-from-windows-universal-apps.md)
    

