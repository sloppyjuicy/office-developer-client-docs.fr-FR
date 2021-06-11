---
title: Lien de l’OSC avec Outlook et les réseaux sociaux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Le connecteur Outlook Social Connector (OSC) peut s’afficher dans la carte de visite Office Outlook et les activités, l’état ou les mises à jour de photos d’un collègue, d’un ami ou de toute personne à qui vous êtes associé.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428010"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>Lien de l’OSC avec Outlook et les réseaux sociaux

Le connecteur Outlook Social Connector (OSC) peut s’afficher dans la carte de visite Office Outlook et les activités, l’état ou les mises à jour de photos d’un collègue, d’un ami ou de toute personne à qui vous êtes associé. Par défaut, l’OSC affiche les messages Outlook, les pièces jointes et les demandes de réunion reçues d’une personne sélectionnée. Si la personne sélectionnée et l’utilisateur Office collaborent sur un site SharePoint, l’OSC affiche également les mises à jour de documents et d’autres activités de site à partir de ce site SharePoint site. Selon les contextes d’association qui intéressent l’utilisateur Office, l’utilisateur Office peut installer des fournisseurs OSC pour des applications métier, des sites web d’entreprise internes ou divers sites de réseaux sociaux et professionnels, tels que LinkedIn, Facebook et Windows Live.
  
Pour prendre en charge le partage de fonctionnalités entre les applications clientes Office, le moteur principal OSC est implémenté dans le cadre d’un composant partagé Office, et le volet Personnes est implémenté en tant que Outlook. Pour utiliser OSC, un utilisateur Office doit avoir installé des Outlook sur cet ordinateur client et configuré des Outlook avec un profil, afin que l’OSC puisse mettre en cache les contacts dans un dossier Contacts. 
  
Un fournisseur OSC est une DLL COM (Component Object Model) qui permet à l’OSC d’accéder aux données de réseau social d’une manière indépendante des API de chaque réseau social. Une DLL de fournisseur OSC doit être installée localement sur un ordinateur client. Le fournisseur OSC d’un réseau social connecte OSC, qui fait partie de Outlook, au réseau social sur Internet.
  
Un fournisseur OSC doit implémenter un ensemble d’interfaces, définies dans le cadre de l’extensibilité du fournisseur OSC, pour communiquer avec l’OSC. L’extensibilité du fournisseur OSC est disponible en tant que plateforme ouverte.
  
L’architecture de fournisseur de l’OSC permet à plusieurs fournisseurs de travailler avec le moteur principal OSC et d’agréger des informations sociales telles que des amis et des activités. La figure 1 illustre l’architecture du fournisseur OSC.
  
**Figure 1. Outlook Architecture du fournisseur Social Connector**

![Réseaux sociaux, fournisseurs OSC, OSC et Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>Terminologie

Dans cette Outlook référence du fournisseur social Connector, un réseau social est utilisé pour faire référence aux types de sites suivants : 
  
- Sites de collaboration tels que SharePoint.
    
- Sites de réseaux sociaux tels que Facebook et Windows Live.
    
- Professional sites réseau tels que LinkedIn.
    
- Autres applications métier ou sites web internes d’entreprise utilisés pour la mise en réseau.
    
Le terme « ami » est généralement utilisé pour inclure des amis, une famille, des collègues, des connexions et toute autre personne à qui un utilisateur Office est associé dans un contexte de collaboration tel que SharePoint, ou a été ajouté au compte de réseau social de l’utilisateur. Les non-amis sont des personnes référencés dans les mises à jour d’activité des amis, mais pas des amis qui ont été ajoutés au compte de réseau social de l’Office de l’utilisateur. Les contacts sont des personnes qui se Outlook dossier de contacts. 
  
## <a name="see-also"></a>Voir aussi

- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

