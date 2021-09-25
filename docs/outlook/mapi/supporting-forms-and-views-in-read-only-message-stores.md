---
title: Prise en charge des formulaires et des affichages dans des magasins de Message en lecture seule
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 688c0726faa5cb27f74f433e356a9931db58033f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590988"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a>Prise en charge des formulaires et des affichages dans des magasins de Message en lecture seule

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si votre fournisseur de banque de messages autorise une autorisation en lecture seule dans le m�canisme de stockage sous-jacent, les applications clientes et le Gestionnaire de formulaire MAPI ne pourront pas effectuer certaines op�rations. En particulier, les clients ne pourront pas ajouter ou modifier des affichages personnalis�s et du Gestionnaire de formulaire MAPI ne pourront pas installer des formulaires dans les tableaux de contenu associ� � des dossiers de la banque.
  
De nombreux magasins de message en lecture seule, qui est peut-�tre pas un probl�me. Si tel est le cas, le fournisseur de banque de messages est inutile prendre en charge les tables de contenu associ�e � tout. Toutefois, si votre fournisseur de banque de messages doit �tre en lecture seule et elle doit �galement prendre en charge un jeu pr�d�fini de vues ou de formulaires, qu'elle a besoin prendre en charge des tableaux de contenu associ�e.
  
La strat�gie la plus courante pour y parvenir, car les clients et le Gestionnaire de formulaire MAPI ne peut pas installer les affichages ou de stockent les formulaires dans le message elle-m�me, est pour le fournisseur de banque de messages pour coder les dans la banque de messages. Cela signifie que le contenu associ� ou des tables qui contiennent les affichages ou les formulaires devant exister dans la banque de messages lors de sa cr�ation, avant les clients ou de l'interface MAPI formulaire Gestionnaire jamais y acc�der. Puis, lorsque le client demande une table de contenu associ�e � obtenir des affichages personnalis�s � partir d'un formulaire ou le Gestionnaire de formulaire MAPI demande une table de contenu associ�e � un formulaire de lancement, le fournisseur de banque de message peut en fournir un. 
  
Cette exigence que les tables des mati�res associ�e cr��s et remplis lors de la cr�ation de la banque de messages proprement dit implique que votre fournisseur de banque de messages devront obtenir des informations sur le format des messages sp�ciaux que les clients et l'interface MAPI forment manager permet de stocker les formulaires et les affichages. Quels sont les formats varient selon le client et le Gestionnaire de formulaire MAPI est utilis�, afin que leur description ne peut pas �tre fournie ici.
  
## <a name="see-also"></a>Voir aussi



[Banques de messages en lecture seule](read-only-message-stores.md)

