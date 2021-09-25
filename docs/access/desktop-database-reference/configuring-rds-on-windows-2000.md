---
title: Configuration de RDS sur Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4c69cdbaf30a2c592790942a04c777b11512631f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565771"
---
# <a name="configuring-rds-on-windows-2000"></a>Configuration RDS sur Windows 2000


**S’applique à** : Access 2013, Office 2013

Si vous rencontrez des difficultés pour faire fonctionner RDS correctement après avoir effectué une mise à niveau vers Windows 2000, suivez les étapes ci-dessous pour tenter de résoudre le problème.

1.  Assurez-vous que le service de publication World Wide Web s’exécute en premier en naviguant vers https://*serveur à* l’aide d’Internet Explorer. Si vous n'êtes pas en mesure de vous connecter de cette manière au serveur Web, ouvrez une invite de commandes et entrez la commande « NET START W3SVC ».

2.  Dans le menu Démarrer, sélectionnez Exécuter. Tapez msdfmap.ini et cliquez sur OK pour ouvrir le fichier msdfmap.ini dans le Bloc-notes. Vérifiez la section CONNECT DEFAULT et, si le paramètre ACCESS est paramétrable \[ \] NOACCESS, changez-le en READONLY.

3.  À l’aide de l’utilitaire RegEdit, accédez à « HKEY LOCAL MACHINE SOFTWARE Microsoft DataFactory HandlerInfo » et assurez-vous que \_ \_ \\ \\ \\ \\ **HandlerRequired**  est définie sur 0 et defaultHandler est « » (chaîne Null).
    
    > [!NOTE]
    > Si vous modifiez cette section du Registre, vous devez redémarrer le service Publication World Wide Web en tapant les commandes « NET STOP W3SVC » puis « NET START W3SVC » à l'invite de commandes.

4.  À l’aide de l’utilitaire RegEdit, accédez au Registre à « HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet Services W3SVC Parameters ADCLaunch » et vérifiez qu’il existe une clé appelée \\ \\ \\ \\ **RDSServer.Datafactory**. Dans le cas contraire, créez-la.

5.  À l’aide du Gestionnaire des services Internet, allez sur le site web par défaut et affichez les propriétés de la racine virtuelle MSADC. Examinez l'onglet Sécurité de répertoire au niveau de la section « Restrictions par adresse IP et nom de domaine ». Si la case à cocher « Accès refusé » est activée, sélectionnez « Accès autorisé ».

Essayez de redémarrer le serveur si ces modifications ne semblent pas résoudre le problème.

