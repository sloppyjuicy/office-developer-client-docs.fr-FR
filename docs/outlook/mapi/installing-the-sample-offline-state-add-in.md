---
title: Installation de l’exemple de add-in d’état hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Last modified: July 06, 2012'
ms.openlocfilehash: f57055c0c9b5651023f110e9540a49382f275696
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630437"
---
# <a name="installing-the-sample-offline-state-add-in"></a>Installation de l’exemple de add-in d’état hors connexion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique vous fait suivre les étapes de téléchargement et d’installation de l’exemple de add-in d’état hors connexion. L’exemple de compl?ment d’état hors ligne est un compl?ment COM qui ajoute un **menu** d’état hors connexion Outlook et utilise l’API d’état hors connexion. Le menu État hors connexion vous permet d’activer ou de désactiver la surveillance de l’état, de vérifier l’état actuel et de modifier l’état actuel. Pour plus d’informations sur la façon dont le add-in d’état hors connexion est implémenté, voir [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).
  
## <a name="install-the-sample-offline-state-add-in"></a>Installer l’exemple de add-in d’état hors connexion

1. Téléchargez l’exemple de add-in d’état hors connexion ici [: Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).
    
2. Exécutez Visual Studio 2005 en tant qu’administrateur.
    
    > [!NOTE]
    > Si votre ordinateur exécute Windows XP, vous devez être connecté en tant qu’administrateur. Si votre ordinateur exécute Windows Vista, vous devez être connecté en tant qu’administrateur. Cliquez avec le bouton droit sur Visual Studio icône 2005 et cliquez **sur Exécuter en tant qu’administrateur.** 
  
3. Dans Visual Studio 2005, cliquez sur **Fichier,** sélectionnez **Ouvrir,** puis cliquez sur **Project/Solution.**
    
4. Accédez à l’emplacement où vous avez enregistré l’exemple, cliquez **sur ConnectionStateAddin,** puis cliquez sur **Ouvrir**.
    
5. Dans le menu **Générer**, cliquez sur **Générer la solution**.
    
6. Dans la **boîte de dialogue Enregistrer le fichier sous,** cliquez sur **Enregistrer.**
    
7. Cliquez sur **le** menu Démarrer, cliquez sur **Tous** les programmes, cliquez sur **Accessoires,** cliquez avec le bouton droit sur Invite de **commandes,** puis cliquez sur Exécuter en **tant qu’administrateur.**
    
    > [!NOTE]
    > Si vous exécutez Windows XP, vous devez être connecté en tant qu’administrateur. 
  
8. Dans la boîte **de dialogue Contrôle de compte** d’utilisateur, cliquez sur **Continuer.**
    
9. Dans la **fenêtre Invite de** commandes, modifiez les répertoires vers le dossier Débogage dans lequel vous avez enregistré l’exemple. Par exemple, si vous avez enregistré l’exemple sur votre C:\ lecteur, vous tapez **cd « C:\ConnectionStateAddin\Debug »,** puis appuyez sur **Entrée**. 
    
10. Tapez **regsvr32 OfflineStateAddin.dll** appuyez sur **Entrée**. 
    
    > [!NOTE]
    > Pour désinstaller l’exemple de add-in d’état hors connexion, tapez **regsvr32 -u OfflineStateAddin.dll**
  
11. Dans la **boîte de dialogue RegSrv32,** cliquez sur **OK.**
    
12. Redémarrez Outlook pour voir le menu **État** hors connexion. 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Installation de l’exemple de complément d’état hors connexion](installing-the-sample-offline-state-add-in.md)
  
[À propos de l’exemple de complément d’état hors connexion](about-the-sample-offline-state-add-in.md)
  
[Configuration d’un complément d’état hors connexion](setting-up-an-offline-state-add-in.md)
  
[Surveillance des modifications de l’état de connexion à l’aide d’un complément d’état hors connexion](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[Déconnexion d’un add-in d’état hors connexion](disconnecting-an-offline-state-add-in.md)

