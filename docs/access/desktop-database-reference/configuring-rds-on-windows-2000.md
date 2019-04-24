---
title: Configuration de RDS sur Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8482df5ca2fab110e5b1a77fe227c5f0c583d893
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296016"
---
# <a name="configuring-rds-on-windows-2000"></a>Configuration RDS sur Windows 2000


**S’applique à** : Access 2013, Office 2013

Si vous rencontrez des difficultés pour faire fonctionner RDS correctement après avoir effectué une mise à niveau vers Windows 2000, suivez les étapes ci-dessous pour tenter de résoudre le problème.

1.  Assurez-vous que le service de publication World World Web est en cours d'exécution en accédant à https://*Server* using Internet Explorer. Si vous n'êtes pas en mesure de vous connecter de cette manière au serveur Web, ouvrez une invite de commandes et entrez la commande « NET START W3SVC ».

2.  Dans le menu Démarrer, sélectionnez Exécuter. Tapez msdfmap.ini et cliquez sur OK pour ouvrir le fichier msdfmap.ini dans le Bloc-notes. Activez la \[case à\] cocher connecter par défaut et, si le paramètre Access a la valeur NoAccess, remplacez-le par ReadOnly.

3.  À l'aide de l'utilitaire RegEdit, accédez\_à\_«\\HKEY\\local\\machine\\Software Microsoft DataFactory HandlerInfo» et assurez-vous que **HandlerRequired** a la valeur 0 et que le **DefaultHandler** est "" (null chaîne).
    
    > [!NOTE]
    > Si vous modifiez cette section du Registre, vous devez redémarrer le service Publication World Wide Web en tapant les commandes « NET STOP W3SVC » puis « NET START W3SVC » à l'invite de commandes.

4.  À l'aide de l'utilitaire RegEdit, accédez au Registre «\_HKEY\_local\\machine\\System\\CurrentControlSet\\services\\W3SVC\\Parameters ADCLaunch» et vérifiez qu'il existe une clé appelée ** RDSServer. DataFactory**. Dans le cas contraire, créez-la.

5.  À l'aide du gestionnaire des services Internet, accédez au site Web par défaut et affichez les propriétés de la racine virtuelle MSADC. Examinez l'onglet Sécurité de répertoire au niveau de la section « Restrictions par adresse IP et nom de domaine ». Si la case à cocher « Accès refusé » est activée, sélectionnez « Accès autorisé ».

Essayez de redémarrer le serveur si ces modifications ne semblent pas résoudre le problème.

