---
title: Prise en charge des formulaires et des affichages dans des magasins de Message en lecture seule
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 0b7ffe07278cfcbba95351f2720e427dd8500221
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350616"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a>Prise en charge des formulaires et des affichages dans des magasins de Message en lecture seule

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si votre fournisseur de banque de messages autorise une autorisation en lecture seule dans le m�canisme de stockage sous-jacent, les applications clientes et le Gestionnaire de formulaire MAPI ne pourront pas effectuer certaines op�rations. En particulier, les clients ne pourront pas ajouter ou modifier des affichages personnalis�s et du Gestionnaire de formulaire MAPI ne pourront pas installer des formulaires dans les tableaux de contenu associ� � des dossiers de la banque.
  
De nombreux magasins de message en lecture seule, qui est peut-�tre pas un probl�me. Si tel est le cas, le fournisseur de banque de messages est inutile prendre en charge les tables de contenu associ�e � tout. Toutefois, si votre fournisseur de banque de messages doit �tre en lecture seule et elle doit �galement prendre en charge un jeu pr�d�fini de vues ou de formulaires, qu'elle a besoin prendre en charge des tableaux de contenu associ�e.
  
La strat�gie la plus courante pour y parvenir, car les clients et le Gestionnaire de formulaire MAPI ne peut pas installer les affichages ou de stockent les formulaires dans le message elle-m�me, est pour le fournisseur de banque de messages pour coder les dans la banque de messages. Cela signifie que le contenu associ� ou des tables qui contiennent les affichages ou les formulaires devant exister dans la banque de messages lors de sa cr�ation, avant les clients ou de l'interface MAPI formulaire Gestionnaire jamais y acc�der. Puis, lorsque le client demande une table de contenu associ�e � obtenir des affichages personnalis�s � partir d'un formulaire ou le Gestionnaire de formulaire MAPI demande une table de contenu associ�e � un formulaire de lancement, le fournisseur de banque de message peut en fournir un. 
  
Cette exigence que les tables des mati�res associ�e cr��s et remplis lors de la cr�ation de la banque de messages proprement dit implique que votre fournisseur de banque de messages devront obtenir des informations sur le format des messages sp�ciaux que les clients et l'interface MAPI forment manager permet de stocker les formulaires et les affichages. Quels sont les formats varient selon le client et le Gestionnaire de formulaire MAPI est utilis�, afin que leur description ne peut pas �tre fournie ici.
  
## <a name="see-also"></a>Voir aussi



[Banques de messages en lecture seule](read-only-message-stores.md)

