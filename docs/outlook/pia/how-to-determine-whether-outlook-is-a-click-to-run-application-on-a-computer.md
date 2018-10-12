---
title: Vérifier si Outlook est une application « Démarrer en un clic » sur un ordinateur
TOCTitle: Determine whether Outlook is a Click-to-Run application on a computer
ms:assetid: 1b8573be-8ea8-4973-869d-87fda57ce525
ms:mtpsurl: https://msdn.microsoft.com/library/Ff522355(v=office.15)
ms:contentKeyID: 55119804
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: c155fed72a314c5c260ed2fe574474afd45c44c3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406651"
---
# <a name="determine-whether-outlook-is-a-click-to-run-application-on-a-computer"></a>Vérifier si Outlook est une application « Démarrer en un clic » sur un ordinateur

« Démarrer en un clic » est un mécanisme de livraison et de mise à jour de logiciels disponible sur Office 2010 et versions ultérieures. Les produits livrés au moyen de « Démarrer en un clic » s’exécutent dans un environnement d’applications virtuelles sur le système d’exploitation local. Cela signifie qu’ils ont des copies privées de leurs fichiers et paramètres, et que les modifications qu’ils apportent sont capturées dans l’environnement virtuel.

Click-to-Run est rapide, les utilisateurs peuvent commencer rapidement à se servir d'une application sans devoir attendre l'installation du produit complet. Les mises à jour s'exécutent automatiquement en arrière-plan, sans que l'utilisateur ne doive d'abord retirer une installation ni procéder manuellement à l'installation des mises à jour. Les produits « Démarrer en un clic » sont virtualisés et ne sont pas en conflit avec d’autres logiciels installés. Cependant, comme un produit livré par « Démarrer en un clic » a des copies privées de tous ses fichiers et de son inscription, un développeur de complément ne peut pas déterminer l’existence du produit de la même manière que pour un produit installé sur le disque dur d’un ordinateur client. À partir d’Outlook 2010, les développeurs de compléments doivent déterminer si Outlook a été installé, et si Outlook a été fourni sous la forme d’un produit « Démarrer en un clic ».


> [!NOTE]
> Seul Office 2013 version 32 bits est pris en charge dans l’environnement d’applications virtuelles « Démarrer en un clic », même si l’ordinateur client utilise un système d’exploitation 64 bits.



### <a name="to-check-whether-outlook-2013-was-delivered-by-click-to-run-on-a-client-computer"></a>Pour vérifier si Outlook 2013 a été fourni par « Démarrer en un clic » sur un ordinateur client, procédez comme suit :

- Vérifiez si la clé VirtualOutlook existe dans l’emplacement suivant du Registre Windows :
    
  `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
    
  La clé VirtualOutlook est une valeur REG\_SZ qui contient la balise culture de la langue installée du produit, par exemple « en-us ».

## <a name="see-also"></a>Voir aussi

- [Administration des compléments](add-in-administration.md)

