---
title: Installation de l’exemple de complément d’état hors connexion
description: L’exemple de complément d’état hors connexion est un complément COM qui ajoute un menu État hors connexion à Outlook et utilise l’API d’état hors connexion.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
ms.openlocfilehash: e3f2884b57d07f85de3e1ab642b896e7de59b69b
ms.sourcegitcommit: 7c1e7389b18d4f067a69b992ac6c876b5e0441b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2022
ms.locfileid: "67365767"
---
# <a name="installing-the-sample-offline-state-add-in"></a>Installation de l’exemple de complément d’état hors connexion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique vous guide tout au long des étapes de téléchargement et d’installation de l’exemple de complément d’état hors connexion. L’exemple de complément d’état hors connexion est un complément COM qui ajoute un menu **État hors connexion** à Outlook et utilise l’API d’état hors connexion. Dans le menu État hors connexion, vous pouvez activer ou désactiver la surveillance de l’état, vérifier l’état actuel et modifier l’état actuel. Pour plus d’informations sur la façon dont le complément d’état hors connexion est implémenté, consultez [Configuration d’un complément d’état hors connexion](setting-up-an-offline-state-add-in.md).
  
## <a name="install-the-sample-offline-state-add-in"></a>Installer l’exemple de complément d’état hors connexion

1. Téléchargez l’exemple de complément d’état hors connexion ici : [Exemples de code de référence auxiliaire Outlook 2007 et Programme d’installation redistribuable](/office/client-developer/outlook/auxiliary/welcome-to-the-outlook-auxiliary-reference).
    
2. Exécutez Visual Studio 2005 en tant qu’administrateur.
    
    > [!NOTE]
    > Si votre ordinateur exécute Windows XP, vous devez être connecté en tant qu’administrateur. Si votre ordinateur exécute Windows Vista, vous devez être connecté en tant qu’administrateur. Cliquez avec le bouton droit sur l’icône Visual Studio 2005, puis cliquez sur **Exécuter en tant qu’administrateur**. 
  
3. Dans Visual Studio 2005, cliquez sur **Fichier**, sélectionnez **Ouvrir**, puis cliquez sur **Projet/Solution**.
    
4. Accédez à l’emplacement où vous avez enregistré l’exemple, cliquez sur **ConnectionStateAddin**, puis sur **Ouvrir**.
    
5. Dans le menu **Générer**, cliquez sur **Générer la solution**.
    
6. Dans la boîte **de dialogue Enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
7. Cliquez sur le menu **Démarrer** , cliquez sur **Tous les programmes**, cliquez sur **Accessoires**, cliquez avec le bouton droit sur **Invite de commandes**, puis cliquez sur **Exécuter en tant qu’administrateur**.
    
    > [!NOTE]
    > Si vous exécutez Windows XP, vous devez être connecté en tant qu’administrateur. 
  
8. Dans la boîte de dialogue **Contrôle de compte d’utilisateur** , cliquez sur **Continuer**.
    
9. Dans la fenêtre **d’invite de commandes** , remplacez les répertoires par le dossier Debug dans lequel vous avez enregistré l’exemple. Par exemple, si vous avez enregistré l’exemple sur votre C:\ lecteur, vous tapez **le cd « C:\ConnectionStateAddin\Debug »,** puis appuyez sur **Entrée**. 
    
10. Tapez **regsvr32 OfflineStateAddin.dll** et **appuyez sur Entrée**. 
    
    > [!NOTE]
    > Pour désinstaller l’exemple de complément d’état hors connexion, tapez **regsvr32 -u OfflineStateAddin.dll**
  
11. Dans la boîte **de dialogue RegSrv32** , cliquez sur **OK**.
    
12. Redémarrez Outlook pour afficher le menu **État hors connexion** . 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Installation de l’exemple de complément d’état hors connexion](installing-the-sample-offline-state-add-in.md)
  
[À propos de l’exemple de complément d’état hors connexion](about-the-sample-offline-state-add-in.md)
  
[Configuration d’un complément d’état hors connexion](setting-up-an-offline-state-add-in.md)
  
[Surveillance des modifications de l’état de connexion à l’aide d’un complément d’état hors connexion](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[Déconnexion d’un complément d’état hors connexion](disconnecting-an-offline-state-add-in.md)

