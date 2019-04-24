---
title: Lien de l’OSC avec Outlook et les réseaux sociaux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook Social Connector (OSC) peut être affiché dans la carte de visite Office et les activités du volet contacts Outlook, État ou mises à jour de photo pour un collègue, un ami ou toute personne à laquelle vous êtes associé.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329255"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>Lien de l’OSC avec Outlook et les réseaux sociaux

Outlook Social Connector (OSC) peut être affiché dans la carte de visite Office et les activités du volet contacts Outlook, État ou mises à jour de photo pour un collègue, un ami ou toute personne à laquelle vous êtes associé. Par défaut, OSC affiche les courriers électroniques, les pièces jointes et les demandes de réunion Outlook reçus d'une personne sélectionnée. Si la personne sélectionnée et l'utilisateur Office collaborent sur un site SharePoint, OSC affiche également les mises à jour de documents et d'autres activités de site à partir de ce site SharePoint. En fonction des contextes d'association qui intéressent l'utilisateur Office, l'utilisateur Office peut installer des fournisseurs OSC pour les applications métier, les sites Web d'entreprise internes ou un large éventail de sites professionnels et de réseaux sociaux, tels que LinkedIn, Facebook et Windows Live.
  
Pour prendre en charge le partage des fonctionnalités dans les applications clientes Office, le moteur de base OSC est implémenté dans le cadre d'un composant partagé Office et le volet de personnes est implémenté en tant que complément Outlook. Pour utiliser le OSC, un utilisateur Office doit avoir installé Outlook sur cet ordinateur client et configuré Outlook avec un profil, afin que le OSC puisse mettre en cache les contacts dans un dossier de contacts. 
  
Un fournisseur OSC est une DLL COM (Component Object Model) qui permet à l'objet OSC d'accéder aux données de réseau social d'une manière indépendante des API de chaque réseau social. Une DLL de fournisseur OSC doit être installée localement sur un ordinateur client. Le fournisseur OSC d'un réseau social connecte le OSC, qui fait partie d'Outlook, avec le réseau social sur Internet.
  
Un fournisseur OSC doit implémenter un ensemble d'interfaces, défini dans le cadre de l'extensibilité du fournisseur OSC, pour communiquer avec le OSC. L'extensibilité du fournisseur OSC est disponible sous forme de plateforme ouverte.
  
L'architecture du fournisseur du OSC permet à plusieurs fournisseurs de travailler avec le moteur de base OSC et d'agréger des informations sociales, telles que des amis et des activités. La figure 1 illustre l'architecture du fournisseur OSC.
  
**Figure 1. Architecture du fournisseur Outlook Social Connector**

![Réseaux sociaux, fournisseurs OSC, OSC et Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>Terminologie

Dans cette référence de fournisseur Outlook Social Connector, un réseau social est utilisé pour faire référence aux types de sites suivants: 
  
- Sites collaboratifs tels que SharePoint.
    
- Sites de réseau social comme Facebook et Windows Live.
    
- Les sites de réseau professionnels tels que LinkedIn.
    
- Autres applications métiers ou sites Web internes d'entreprise utilisés pour la mise en réseau.
    
Le terme Friend est généralement utilisé pour inclure les amis, la famille, les collègues, les connexions et tout autre utilisateur auquel un utilisateur Office est associé dans un contexte collaboratif tel que SharePoint, ou qui a été ajouté au compte de réseau social de l'utilisateur. Les non-amis sont des personnes référencées dans les mises à jour des activités des amis, mais pas des amis qui ont été ajoutés au compte de réseau social de l'utilisateur Office. Les contacts sont des personnes dans un dossier de contacts Outlook. 
  
## <a name="see-also"></a>Voir aussi

- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

