---
title: Configuration de RDS sur Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80ce29ed129035dcb6799844a4b78509b976f0ee
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862939"
---
# <a name="configuring-rds-on-windows-2000"></a>Configuration de RDS sur Windows 2000


**S’applique à**: Access 2013 | Office 2013

Si vous rencontrez des difficultés pour faire fonctionner RDS correctement après avoir effectué une mise à niveau vers Windows 2000, suivez les étapes ci-dessous pour tenter de résoudre le problème.

1.  Assurez-vous que le premier que le Service de publication World Wide Web est en cours d’exécution en accédant à https://*server* à l’aide d’Internet Explorer. Si vous n'êtes pas en mesure de vous connecter de cette manière au serveur Web, ouvrez une invite de commandes et entrez la commande « NET START W3SVC ».

2.  Dans le menu Démarrer, sélectionnez Exécuter. Tapez msdfmap.ini et cliquez sur OK pour ouvrir le fichier msdfmap.ini dans le Bloc-notes. Vérifier la \[CONNECT DEFAULT\] section et si le paramètre d’accès est défini sur NOACCESS, modifiez-la en READONLY.

3.  À l’aide de l’utilitaire RegEdit, accédez à « HKEY\_LOCAL\_ordinateur\\logiciel\\Microsoft\\DataFactory\\HandlerInfo » et assurez-vous que **HandlerRequired** a la valeur 0 et **que DefaultHandler** correspond « » (Null chaîne).
    
    > [!NOTE]
    > [!REMARQUE] Si vous modifiez cette section du Registre, vous devez redémarrer le service Publication World Wide Web en tapant les commandes « NET STOP W3SVC » puis « NET START W3SVC » à l'invite de commandes.

4.  À l’aide de l’utilitaire RegEdit, accédez à dans le registre » HKEY\_LOCAL\_ordinateur\\système\\CurrentControlSet\\Services\\W3SVC\\paramètres\\ADCLaunch » et vérifiez qu’il existe une clé **appelé RDSServer.Datafactory**. Dans le cas contraire, créez-la.

<<<<<<< EN-TÊTE
5.  En utilisant le gestionnaire des services Internet, accédez au Site Web par défaut et affichez les propriétés de la racine virtuelle MSADC. Examinez l'onglet Sécurité de répertoire au niveau de la section « Restrictions par adresse IP et nom de domaine ». Si la case à cocher « Accès refusé » est activée, sélectionnez « Accès autorisé ».
=======
5.  À l’aide du Gestionnaire des Services Internet, accédez au site Web par défaut et afficher les propriétés de la racine virtuelle MSADC. Examinez l'onglet Sécurité de répertoire au niveau de la section « Restrictions par adresse IP et nom de domaine ». Si la case à cocher « Accès refusé » est activée, sélectionnez « Accès autorisé ».
>>>>>>> master

Essayez de redémarrer le serveur si ces modifications ne semblent pas résoudre le problème.

