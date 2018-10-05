---
title: Installation de l’exemple de complément d’état hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Dernière modification : 06 juillet 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389196"
---
# <a name="installing-the-sample-offline-state-add-in"></a>Installation de l’exemple de complément d’état hors connexion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique présente les étapes pour télécharger et installer le complément exemple hors connexion état. Le complément exemple hors connexion état est un complément COM qui ajoute un menu **État hors connexion** dans Outlook et utilise l’API de l’état en mode hors connexion. Via le menu état hors connexion, vous pouvez activer ou désactiver l’analyse de l’état, vérifiez l’état actuel et modifier l’état actuel. Pour plus d’informations sur la façon dont le complément état hors connexion est implémenté, voir [définition d’une en mode hors connexion de l’état Add-in](setting-up-an-offline-state-add-in.md).
  
## <a name="install-the-sample-offline-state-add-in"></a>Installer l’exemple en mode hors connexion d’état complément

1. Télécharger l’exemple hors connexion état complément ici : [exemples de Code de référence Outlook 2007 supplémentaire et programme d’installation redistribuable](https://www.microsoft.com/en-us/download/details.aspx?id=24102).
    
2. Exécutez Visual Studio 2005 en tant qu’administrateur.
    
    > [!NOTE]
    > Si votre ordinateur exécute Windows XP, vous devez être connecté en tant qu’administrateur. Si votre ordinateur exécute Windows Vista, vous devez être connecté en tant qu’administrateur. Cliquez sur l’icône de Visual Studio 2005, cliquez sur **Exécuter en tant qu’administrateur**. 
  
3. Dans Visual Studio 2005, cliquez sur **fichier**, sélectionnez **Ouvrir**, puis cliquez sur **Projet/Solution**.
    
4. Accédez à l’emplacement où vous avez enregistré l’exemple et cliquez sur **ConnectionStateAddin**, puis cliquez sur **Ouvrir**.
    
5. On the **Build** menu, click **Build Solution**.
    
6. Dans la boîte de dialogue **Enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
7. Cliquez sur le menu **Démarrer** , sur **Tous les programmes**, sur **Accessoires**, avec le bouton droit **invite de commandes**, puis cliquez sur **Exécuter en tant qu’administrateur**.
    
    > [!NOTE]
    > Si vous exécutez Windows XP, vous devez être connecté en tant qu’administrateur. 
  
8. Dans la boîte de dialogue **Contrôle de compte d’utilisateur** , cliquez sur **Continuer**.
    
9. Dans la fenêtre **d’invite de commandes** , accédez au dossier où vous avez enregistré l’exemple Debug. Par exemple, si vous avez enregistré l’exemple sur votre lecteur C:\, vous souhaite tapez **cd « C:\ConnectionStateAddin\Debug »** , puis appuyez sur **entrée**. 
    
10. Tapez **regsvr32 OfflineStateAddin.dll** et appuyez sur **entrée**. 
    
    > [!NOTE]
    > Pour désinstaller le complément exemple hors connexion état, tapez **regsvr32-u OfflineStateAddin.dll**
  
11. Dans la boîte de dialogue **RegSrv32** , cliquez sur **OK**.
    
12. Redémarrez Outlook pour afficher le menu **d’État hors connexion** . 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Installation de l’exemple de complément d’état hors connexion](installing-the-sample-offline-state-add-in.md)
  
[À propos de l’exemple de complément d’état hors connexion](about-the-sample-offline-state-add-in.md)
  
[Configuration d’un complément d’état hors connexion](setting-up-an-offline-state-add-in.md)
  
[Surveillance des modifications de l’état de connexion à l’aide d’un complément d’état hors connexion](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[Déconnexion d’un complément d’état hors connexion](disconnecting-an-offline-state-add-in.md)

