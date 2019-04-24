---
title: Installation de l'exemple de complément d'État hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Dernière modification: juillet 06, 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317212"
---
# <a name="installing-the-sample-offline-state-add-in"></a>Installation de l'exemple de complément d'État hors connexion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique décrit les étapes à suivre pour télécharger et installer l'exemple de complément d'État hors connexion. L'exemple de complément d'État hors connexion est un complément COM qui ajoute un menu d' **État hors** connexion à Outlook et utilise l'API d'État hors connexion. Le menu État hors connexion vous permet d'activer ou de désactiver l'analyse de l'État, de vérifier l'état actuel et de modifier l'état actuel. Pour plus d'informations sur la façon dont le complément d'État hors connexion est implémenté, consultez la rubrique [configuration d'un complément d'État hors connexion](setting-up-an-offline-state-add-in.md).
  
## <a name="install-the-sample-offline-state-add-in"></a>Installer l'exemple de complément d'État hors connexion

1. Téléchargez l'exemple de complément d'État hors connexion ici: [exemples de code de référence auxiliaire Outlook 2007 et programme d'installation](https://www.microsoft.com/en-us/download/details.aspx?id=24102)redistribuable.
    
2. Exécutez Visual Studio 2005 en tant qu'administrateur.
    
    > [!NOTE]
    > Si votre ordinateur fonctionne sous Windows XP, vous devez être connecté en tant qu'administrateur. Si votre ordinateur exécute Windows Vista, vous devez être connecté en tant qu'administrateur. Cliquez avec le bouton droit sur l'icône Visual Studio 2005, puis cliquez sur **exécuter en tant qu'administrateur**. 
  
3. Dans Visual Studio 2005, cliquez sur **fichier**, sur **ouvrir**, puis sur **projet/solution**.
    
4. Naviguez jusqu'à l'emplacement où vous avez enregistré l'exemple, cliquez sur **ConnectionStateAddin**, puis cliquez sur **ouvrir**.
    
5. Dans le menu **Générer**, cliquez sur **Générer la solution**.
    
6. Dans la boîte de dialogue **enregistrer le fichier sous** , cliquez sur **Enregistrer**.
    
7. Cliquez sur le menu **Démarrer** , cliquez sur **tous les programmes**, cliquez sur **accessoires**, cliquez avec le bouton droit sur **invite de commandes**, puis cliquez sur **exécuter en tant qu'administrateur**.
    
    > [!NOTE]
    > Si vous exécutez Windows XP, vous devez être connecté en tant qu'administrateur. 
  
8. Dans la boîte de dialogue **contrôle de compte d'utilisateur** , cliquez sur **Continuer**.
    
9. Dans la fenêtre d' **invite de commandes** , accédez au dossier de débogage dans lequel vous avez enregistré l'exemple. Par exemple, si vous avez enregistré l'exemple sur le C:\ tapez **CD «C:\ConnectionStateAddin\Debug»** , puis appuyez sur **entrée**. 
    
10. Tapez **regsvr32 OfflineStateAddin. dll** , puis appuyez sur **entrée**. 
    
    > [!NOTE]
    > Pour désinstaller l'exemple de complément d'État hors connexion, tapez **regsvr32-u OfflineStateAddin. dll**
  
11. Dans la boîte de dialogue **Regsrv32** , cliquez sur **OK**.
    
12. ReDémarrez Outlook pour afficher le menu **État hors connexion** . 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
  
[Installation de l’exemple de complément d’état hors connexion](installing-the-sample-offline-state-add-in.md)
  
[À propos de l’exemple de complément d’état hors connexion](about-the-sample-offline-state-add-in.md)
  
[Configuration d’un complément d’état hors connexion](setting-up-an-offline-state-add-in.md)
  
[Surveillance des modifications de l’état de connexion à l’aide d’un complément d’état hors connexion](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[Déconnexion d'un complément d'État hors connexion](disconnecting-an-offline-state-add-in.md)

