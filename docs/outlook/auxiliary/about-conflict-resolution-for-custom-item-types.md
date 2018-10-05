---
title: À propos de la résolution de conflit pour les types d’éléments personnalisés
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 3f0853fc-f9f2-4314-ac55-47fe1e52d019
description: Cette rubrique décrit comment résoudre les conflits pour les types d’élément personnalisé que vous créez dans Outlook.
ms.openlocfilehash: 357dd9182f26c4e9e1e264afdee296859e7b3483
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382987"
---
# <a name="about-conflict-resolution-for-custom-item-types"></a>À propos de la résolution de conflit pour les types d’éléments personnalisés

Cette rubrique décrit comment résoudre les conflits pour les types d’élément personnalisé que vous créez dans Outlook.
  
## <a name="conflict-resolution-for-standard-outlook-item-types"></a>Résolution de conflit pour les types d’éléments Outlook standards

Dans Outlook, les conflits se produisent lorsque deux ou plusieurs copies du même article ont été modifiés indépendamment les uns des autres. Outlook détecte des conflits lors de la synchronisation. Par exemple, vous pourrez mettre à jour un élément de réunion en ligne dans Outlook Web App et puis mettre à jour le même élément de réunion dans Outlook lorsque vous travaillez en mode hors connexion. Lorsque Outlook est en ligne à nouveau et synchronise les données entre l’ordinateur client et le serveur, elle détecte qu’il existe deux copies de l’élément de réunion même.
  
Lorsque Outlook synchronise les éléments qui appartiennent à un type d’élément Outlook standard, il prend en considération les propriétés qui sont spécifiques à ce type d’élément pour détecter les conflits possibles. Outlook tente de résoudre les conflits et stocke la copie résultante dans le dossier approprié sans demander l’intervention de l’utilisateur. Dans les cas où Outlook considère qu’il est possible que la copie résultante ne peut pas contenir toutes les données essentielles, Outlook stocke les copies en conflit dans le dossier conflits, sous le dossier problèmes de synchronisation. 
  
> [!NOTE]
> Problèmes de synchronisation et ses sous-dossiers sont masqués jusqu'à ce que vous cliquez sur **Liste des dossiers** dans le volet de Navigation. 
  
Dans ce cas, les utilisateurs peuvent choisir accéder au dossier conflits pour vérifier les éléments qui ont été en conflit et s’il faut utiliser une copie dans le dossier conflits pour remplacer la copie Outlook a décidé de conserver.
  
## <a name="conflict-resolution-for-custom-item-types"></a>Résolution de conflit pour les types d’éléments personnalisés

### <a name="item-types-and-message-classes"></a>Types d’éléments et classes de message
  
Tous les éléments Outlook sont associés à une classe de message. Par exemple, par défaut, un élément de messagerie est associé à la classe de message **IPM. Remarque**. La classe de message est principalement utilisée pour identifier le formulaire doit être utilisé pour afficher l’élément dans Outlook. Outlook prend en charge une liste des classes de message qui sont mappées sur les types d’éléments intégrées à Outlook. Pour plus d’informations sur les classes de message, reportez-vous à la rubrique [Types d’éléments et classes de messages](https://msdn.microsoft.com/library/15b709cc-7486-b6c7-88a3-4a4d8e0ab292%28Office.15%29.aspx). 
  
Utilisateurs peuvent créer des types d’éléments personnalisés, assigner des classes de message personnalisées pour les types d’éléments personnalisés et qu’Outlook à utiliser un formulaire personnalisé pour afficher les types d’éléments personnalisés. Par exemple, vous souhaiterez Outlook d’afficher un formulaire de contact personnalisé d’entreprise pour vos contacts professionnels. Pour cela, vous pouvez créer une classe de message personnalisée **IPM. Contact.Business**, créez un formulaire personnalisé pour cette classe de message et affecter des contacts professionnels avec cette classe de message. 
  
### <a name="registering-a-conflict-resolution-scheme-for-custom-item-types"></a>Inscription d’un schéma de résolution de conflit pour les types d’élément personnalisé
  
Lorsque vous créez un type d’élément personnalisé, autre que la classe de message et le formulaire personnalisé, vous devez également envisager la façon dont vous voulez qu’Outlook pour gérer les conflits entre les copies d’un élément de ce type d’élément. Par défaut, Outlook utilise un schéma de résolution commun à tous les éléments, ne tient pas compte des propriétés qui sont spécifiques à un type d’élément et présente les copies en conflit à l’utilisateur de prendre une décision. Il s’agit, car les types d’élément personnalisé peuvent définir des champs personnalisés dans le formulaire personnalisé et peuvent avoir des propriétés personnalisées et code personnalisé. Si vous souhaitez prendre en compte les propriétés propres à l’élément et de tenter de résoudre le conflit avec une intervention minimale de l’utilisateur d’Outlook, vous devez spécifier que via un paramètre dans le Registre Windows. Il est possible de deux façons : 
  
- En appliquant un paramètre de stratégie de groupe sur l’ordinateur local qui définit la clé de Registre ConflictMsgCls. L’exemple suivant indique la version « 14.0 » pour Outlook 2010 : 
  
   `[HKCU]\Software\Policies\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
- En modifiant directement la clé de Registre utilisateur ConflictMsgCls. L’exemple suivant indique la version « 14.0 » pour Outlook 2010 : 
  
   `[HKCU]\Software\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
Définition de la résolution de conflit par le biais de la stratégie de groupe est prioritaire sur modifiant directement la clé de Registre utilisateur. L’emplacement de la clé de Registre dépend de la version d’Outlook. Vous spécifiez le nom de la classe de message personnalisé en tant que valeur sous cette clé. Spécifiez le type de la valeur **DWORD**et les données de la valeur, comme une des valeurs indiquées dans le tableau suivant, selon le schéma de résolution que vous choisissez. 
  
|Data  | Description  |
|:-----|:-----|
|0  <br/> |Résolution élément courantes nécessitant une décision de l’utilisateur, tel qu’utilisé dans Outlook 2002 et les versions antérieures.  <br/> |
|1  <br/> |Résolution élément courants qui nécessite une intervention minimale de l’utilisateur, comme dans Outlook depuis Outlook 2003.  <br/> |
|2  <br/> |Résolution spécifique aux éléments de courrier.  <br/> |
|3  <br/> |Résolution spécifique aux éléments de la réunion.  <br/> |
|4  <br/> |Résolution spécifique aux éléments de rendez-vous.  <br/> |
|5  <br/> |Résolution des éléments de contact.  <br/> |
|6  <br/> |Résolution spécifique aux éléments de tâche.  <br/> |
|7  <br/> |Résolution spécifique aux éléments pense-bête.  <br/> |
|8  <br/> |Résolution spécifique aux éléments de journal.  <br/> |
   
Si vous spécifiez un des modes de résolution propres à l’élément (clées données 2 à 8), Outlook essaie de résoudre les conflits dans les champs propres à l’élément (par exemple, les champs **début** et **fin** d’un élément de rendez-vous) automatiquement sans intervention de l’utilisateur . Si Outlook estime que la résolution peut entraîner la perte de données essentielles, Outlook conserve des copies en conflit dans le dossier conflits et utilisateurs peuvent choisir d’accéder au dossier conflits pour résoudre ces éléments et remplacer automatique manuellement résolution. 
  
À l’aide de l’exemple de contacts professionnels même ci-dessus, si vous souhaitez spécifier le schéma de résolution de propres à l’élément contact pour la classe de message **IPM. Contact.Business**, vous pouvez l’ajouter comme une valeur **DWORD** sous `[HKCU]\Software\Microsoft\Office\15.0\Outlook\Options\ConflictMsgCls`et spécifiez 5 comme les données. 
  
> [!NOTE]
> Outlook utilise toujours un schéma de résolution spécifiques à des éléments de rendez-vous pour les classes de message personnalisées qui reposent sur la classe de message de rendez-vous, **IPM. Rendez-vous** (par exemple, **IPM. Appointment.Personal**). 
  
## <a name="see-also"></a>Voir aussi

- [Éléments Outlook](https://msdn.microsoft.com/library/6ea4babf-facf-4018-ef5a-4a484e55153a%28Office.15%29.aspx)

