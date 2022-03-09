---
title: Prise en charge de plusieurs clients l'acc�s aux Messages dans les banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 31885c64-edb2-4a87-8730-09f163dedd40
ms.openlocfilehash: 11587b748f896bf8b3f25823ed438904b34ad9fb
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379317"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a>Prise en charge de plusieurs clients l'acc�s aux Messages dans les banques de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il est possible pour plusieurs applications clientes ouvrir un message donn� simultan�ment. Fournisseurs de banque de messages n'ont pas � suivre toutes les r�gles de gouvernance de ce type d'acc�s particuliers. Toutefois, si les applications clientes modifier le message et enregistrement leurs modifications, le fournisseur de magasins doit respecter les avec les r�gles suivantes :
  
- Autoriser le premier appel � la m�thode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) afin de passer comme s'il �tait le seul client o� le message est ouvert. 
    
- Dans les appels suivants **SaveChanges** par d'autres clients, le fournisseur de banque de messages doit ignorer les modifications et retourner MAPI_E_OBJECT_CHANGED. 
    
- Permettent aux applications clientes r�pondre � un code de retour MAPI_E_OBJECT_CHANGED en appelant **SaveChanges** � l'aide de l'indicateur FORCE_SAVE. Si une application cliente effectue cette action, le fournisseur de banque de messages doit remplacer les modifications pr�c�dentes avec les nouveaux. 
    
Sinon, le fournisseur de banque de messages peut d�tecter le conflit et pr�sentent une interface qui permet � l'utilisateur de choisir s'il faut conserver le message d'origine, remplacer le message d'origine avec les nouvelles modifications ou enregistrer les modifications apport�es � un autre emplacement.
  
## <a name="see-also"></a>Voir aussi



[Implémentation des messages dans les banques de messages](implementing-messages-in-message-stores.md)

