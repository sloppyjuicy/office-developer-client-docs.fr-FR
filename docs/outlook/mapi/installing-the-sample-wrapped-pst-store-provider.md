---
title: Installation de l'exemple de fournisseur de magasins PST encapsulé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: a1574de555eb74d06c4dbe721e7e013ac59d3071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309631"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a>Installation de l'exemple de fournisseur de magasins PST encapsulé

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique décrit les étapes à suivre pour télécharger et installer l'exemple de fournisseur de banque d'informations PST encapsulé. L'exemple de fournisseur de banque de fichiers PST encapsulé, WrapPST, implémente un fournisseur de magasins PST encapsulé destiné à être utilisé conjointement avec l'API de réPlication. Pour plus d'informations sur l'API de réPlication, voir [à propos de l'API](about-the-replication-api.md)de réplication.
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a>Installer l'exemple de fournisseur de magasins PST encapsulé

1. Pour télécharger l'exemple de fournisseur de magasins PST encapsulé, voir [exemples de code de référence auxiliaire Outlook 2007 et programme d'installation](https://www.microsoft.com/en-us/download/details.aspx?id=24102)redistribuable.
    
2. Ouvrez le dossier **SampleWrappedPSTStoreProvider** , puis cliquez sur **extraire tous les fichiers**.
    
3. Cliquez sur **Parcourir**, sélectionnez l'emplacement où vous souhaitez enregistrer l'exemple, puis cliquez sur **OK**.
    
4. Cliquez sur **Extraire**.  Le dossier que vous avez sélectionné apparaît et contient les fichiers extraits.
    
5. Ouvrez Visual Studio 2005 en tant qu'administrateur.
    
    > [!NOTE]
    > Si votre ordinateur fonctionne sous Windows XP, vous devez être connecté en tant qu'administrateur. Si votre ordinateur exécute Windows Vista, vous devez être connecté en tant qu'administrateur et vous devez cliquer avec le bouton droit sur l'icône Visual Studio 2005 et cliquer sur **exécuter en tant qu'administrateur**. 
  
6. Dans Visual Studio 2005, cliquez sur **fichier**, sur **ouvrir**, puis sur **projet/solution**.
    
7. Naviguez jusqu'à l'emplacement où vous avez enregistré l'exemple, cliquez sur **WrapPST**, puis cliquez sur **ouvrir**.
    
8. Dans le menu **Générer**, cliquez sur **Générer la solution**.
    
9. Dans la boîte de dialogue **enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
10. Dans le dossier où vous avez enregistré l'exemple, cliquez avec le bouton droit sur le fichier **install. bat** , puis cliquez sur **exécuter en tant qu'administrateur**.
    
11. Dans la boîte de dialogue **contrôle de compte d'utilisateur** , cliquez sur **Continuer**.
    
## <a name="see-also"></a>Voir aussi



[À propos de l'exemple de fournisseur de banque d'informations PST encapsulé](about-the-sample-wrapped-pst-store-provider.md)
  
[Initialisation d'un fournisseur de magasins PST encapsulé](initializing-a-wrapped-pst-store-provider.md)
  
[Connexion à un fournisseur de magasins PST encapsulé](logging-on-to-a-wrapped-pst-store-provider.md)
  
[Utilisation d'un fournisseur de magasins PST encapsulé](using-a-wrapped-pst-store-provider.md)
  
[Arrêt d'un fournisseur de magasins PST encapsulé](shutting-down-a-wrapped-pst-store-provider.md)

