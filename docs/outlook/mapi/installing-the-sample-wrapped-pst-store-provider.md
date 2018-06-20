---
title: Installation de l’exemple de wrapper fournisseur de banque de dossiers personnels
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: 29aabc7a2e8513bf24bd3b56ff3e4a126e3d7437
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784319"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a>Installation de l’exemple de wrapper fournisseur de banque de dossiers personnels

  
  
**S’applique à**: Outlook 
  
Cette rubrique présente les étapes pour télécharger et installer le fournisseur de banque exemple encapsulé PST. L’exemple encapsulé PST stocker de fournisseur, WrapPST, implémente un fournisseur de banque PST encapsulé est destiné à être utilisé conjointement avec l’API de réplication. Pour plus d’informations sur l’API de réplication, consultez la rubrique [Sur l’API de réplication](about-the-replication-api.md).
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a>Installer l’exemple de fournisseur de banque de dossiers personnels encapsulé

1. Pour télécharger le fournisseur de banque exemple encapsulé PST, voir [exemples de Code de référence Outlook 2007 supplémentaire et programme d’installation redistribuable](http://www.microsoft.com/en-us/download/details.aspx?id=24102).
    
2. Ouvrez le dossier **SampleWrappedPSTStoreProvider** , puis cliquez sur **Extraire tous les fichiers**.
    
3. Cliquez sur **Parcourir**, sélectionnez l’emplacement où vous souhaitez enregistrer l’exemple et cliquez sur **OK**.
    
4. Cliquez sur **Extraire**. Le dossier que vous avez sélectionné apparaît et contient les fichiers extraits.
    
5. Ouvrez Visual Studio 2005 en tant qu’administrateur.
    
    > [!NOTE]
    > Si votre ordinateur exécute Windows XP, vous devez être connecté en tant qu’administrateur. Si votre ordinateur exécute Windows Vista, vous devez être connecté en comme un administrateur et que vous devez avec le bouton droit de l’icône de Visual Studio 2005, cliquez sur **Exécuter en tant qu’administrateur**. 
  
6. Dans Visual Studio 2005, cliquez sur **fichier**, sélectionnez **Ouvrir**, puis cliquez sur **Projet/Solution**.
    
7. Accédez à l’emplacement où vous avez enregistré l’exemple et cliquez sur **WrapPST**, puis cliquez sur **Ouvrir**.
    
8. On the **Build** menu, click **Build Solution**.
    
9. Dans la boîte de dialogue **Enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
10. Dans le dossier où vous avez enregistré l’exemple, cliquez sur le fichier **Install.bat** et cliquez sur **Exécuter en tant qu’administrateur**.
    
11. Dans la boîte de dialogue **Contrôle de compte d’utilisateur** , cliquez sur **Continuer**.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’exemple de wrapper fournisseur de banque de dossiers personnels](about-the-sample-wrapped-pst-store-provider.md)
  
[L’initialisation d’un fournisseur de banque de dossiers personnels encapsulé](initializing-a-wrapped-pst-store-provider.md)
  
[Se connecter à un fournisseur de banque de dossiers personnels encapsulé](logging-on-to-a-wrapped-pst-store-provider.md)
  
[À l’aide d’un fournisseur de banque de dossiers personnels encapsulé](using-a-wrapped-pst-store-provider.md)
  
[Arrêt d’un fournisseur de banque de dossiers personnels encapsulé](shutting-down-a-wrapped-pst-store-provider.md)

