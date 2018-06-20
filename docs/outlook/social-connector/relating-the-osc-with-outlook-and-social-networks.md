---
title: Concernant l’OSC avec Outlook et les réseaux sociaux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: L’Outlook Social Connector (OSC) peut afficher dans le volet personnes d’Outlook et de la carte de visite Office activités, état ou mises à jour de la photo d’un collègue, friend ou toute personne qui que vous sont associés.
ms.openlocfilehash: 6dc6221b89eca5303e7cf6a201927659d4ac9107
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787708"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>Concernant l’OSC avec Outlook et les réseaux sociaux

L’Outlook Social Connector (OSC) peut afficher dans le volet personnes d’Outlook et de la carte de visite Office activités, état ou mises à jour de la photo d’un collègue, friend ou toute personne qui que vous sont associés. Par défaut, l’OSC affiche les courriers électroniques Outlook, les pièces jointes, et les demandes de réunion provenant d’une personne sélectionnée. Si la personne sélectionnée et que l’utilisateur Office collaborent sur un site SharePoint, l’OSC affiche également les mises à jour du document et autres activités de site à partir de ce site SharePoint. Selon les contextes d’association est intéressée par l’utilisateur d’Office, l’utilisateur d’Office peut installer fournisseurs OSC line-of-business applications, des sites Web d’entreprise internes ou une variété de sites de réseau social Professionnel, tels que LinkedIn, Facebook et Windows Live.
  
Pour prendre en charge le partage des fonctionnalités entre les applications clientes Office, le moteur de base OSC est implémenté dans le cadre d’un composant partagé d’Office et le volet personnes est implémenté sous la forme d’un complément Outlook. Pour utiliser l’OSC, un utilisateur d’Office doit avoir installé Outlook sur l’ordinateur client et configurer Outlook avec un profil, afin que l’OSC peut mettre en cache les contacts d’un dossier Contacts. 
  
Un fournisseur OSC est un composant COM (Object Model) DLL qui permet à l’OSC accéder aux données de réseau social de façon indépendante des API de chaque réseau social. Un fournisseur OSC DLL doit être installé localement sur un ordinateur client. Fournisseur OSC d’un réseau social connecte OSC, ce qui fait partie d’Outlook, avec le réseaux sociaux sur Internet.
  
Un fournisseur OSC doit implémenter un ensemble d’interfaces, définies dans le cadre de l’extensibilité de fournisseur OSC, de communiquer avec l’OSC. Extensibilité du fournisseur OSC est disponible comme une plate-forme ouverte.
  
L’architecture du fournisseur de l’OSC permet de plusieurs fournisseurs travailler avec le moteur de base OSC et compilent les informations telles que des amis et activités sociales. La figure 1 illustre l’architecture de fournisseur OSC.
  
**La figure 1. Architecture du fournisseur Outlook Social Connector**

![Réseaux sociaux, fournisseurs OSC, OSC et Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>Terminologie

Dans cette référence Outlook Social Connector fournisseur, un réseau social est utilisé pour faire référence aux types de sites suivants : 
  
- Sites de collaboration tels que SharePoint.
    
- Sites de réseau social tel que Facebook et Windows Live.
    
- Sites de réseau professionnel tels que LinkedIn.
    
- Autres applications métier d’ou entreprise internes sites Web utilisés pour la mise en réseau.
    
Votre ami termes est généralement utilisé pour inclure des amis, famille, collègues, les connexions et quiconque un utilisateur d’Office est associée dans un contexte de collaboration tels que SharePoint, ou a ajouté au compte de réseau social de l’utilisateur. Non-amis sont les personnes référencées dans les mises à jour des activités de vos amis, mais ne sont pas des amis qui ont été ajoutés au compte de réseau social de l’utilisateur d’Office. Les contacts sont des personnes dans un dossier de contacts Outlook. 
  
## <a name="see-also"></a>Voir aussi

- [Prise en main du développement d'un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

