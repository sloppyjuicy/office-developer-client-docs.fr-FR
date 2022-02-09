---
title: Copie ou déplacement d’un message ou dossier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: e04b9d6b75512308c060d709fc11dd1aa96c5fb7
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462508"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>Copie ou déplacement d’un message ou dossier
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un client peut utiliser l’une des quatre méthodes pour copier ou déplacer un message ou un dossier :
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
En paramétrez les indicateurs et paramètres appropriés pour que **CopyTo** et **CopyProps** fonctionnent comme **CopyFolder** ou **CopyMessages**. Prenons en compte les problèmes suivants lors du choix de la méthode à appeler :
  
- Copiez-vous ou déplacez-vous un dossier ou un message ?
    
- Que savez-vous du dossier ou du message à déplacer ou à copier ?
    
- Combien de propriétés du dossier ou du message seront déplacées ou copiées ?
    
Vous pouvez utiliser les **méthodes IMAPIProp** pour copier ou déplacer un dossier ou un message. **IMAPIFolder::CopyMessages** fonctionne uniquement avec les messages ; **IMAPIFolder::CopyFolder** fonctionne uniquement avec les dossiers. 
  
Alors que l’utilisation des méthodes **IMAPIFolder** ne nécessite aucune connaissance des propriétés prise en charge par le dossier ou le message à copier ou déplacer, vous devez avoir quelques connaissances pour utiliser les méthodes **IMAPIProp** . Avec **IMAPIProp::CopyProps**, vous devez être en mesure de spécifier explicitement quelles propriétés de dossier ou de message vous souhaitez copier ou déplacer. Avec **IMAPIProp::CopyTo**, sauf si vous souhaitez copier ou déplacer toutes les propriétés, vous devez spécifier explicitement les propriétés qui doivent être exclues. Pour plus d’informations sur ces méthodes, voir [Copie des propriétés MAPI](copying-mapi-properties.md).
  
Le nombre de propriétés à copier ou à déplacer peut affecter votre décision quant à la méthode à utiliser. Si vous copiez ou déplacez plusieurs messages, appelez **IMAPIFolder::CopyMessages**. Un autre choix consiste à appeler **IMAPIProp::CopyProps** pour copier uniquement la propriété **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) du dossier. La procédure suivante montre comment utiliser **CopyMessages**. 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>Pour copier ou déplacer un ou plusieurs messages
  
1. Recherchez les identificateurs d’entrée valides pour les dossiers source et de destination.
    
2. Ouvrez ces dossiers en mode lecture/écriture en appelant [IMAPISession::OpenEntry](imapisession-openentry.md) ou [IMsgStore::OpenEntry](imsgstore-openentry.md) et en MAPI_MODIFY’indicateur. 
    
3. Vérifiez que le pointeur d’interface renvoyé par **OpenEntry** est un **pointeur d’interface IMAPIFolder** . Si ce n’est pas le cas, cast vers le type LPMAPIFOLDER. 
    
4. Créez un tableau d’identificateurs d’entrée représentant un ou plusieurs messages à copier ou déplacer. 
    
5. **Appelez IMAPIFolder::CopyMessages** avec les indicateurs suivants : 
    
   - MESSAGE_MOVE, si vous souhaitez effectuer une opération de déplacement. 
    
   - MESSAGE_DIALOG et passez une poignée de fenêtre dans le paramètre _ulUIParam_ , si vous souhaitez que le dossier affiche un indicateur de progression. 
    
6. Relâchez les pointeurs **IMAPIFolder** pour les dossiers source et de destination. 
    
Si vous souhaitez copier le contenu complet d’un dossier dans un autre dossier, appelez la méthode **IMAPIFolder::CopyFolder** ou **IMAPIProp::CopyTo** du dossier source. 
  
Pour copier quelques-unes des propriétés d’un dossier, appelez sa méthode **IMAPIProp::CopyProps** . Pour copier la plupart des propriétés d’un dossier, appelez **IMAPIProp::CopyTo**. 
  
Par exemple, si vous souhaitez copier les propriétés **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) d’un dossier, vous avez les options suivantes :
  
- Appelez **IMAPIFolder::CopyFolder** pour copier toutes les propriétés du dossier, puis supprimez les propriétés indésirables du nouveau dossier. 
    
- **Appelez CopyTo** et excluez toutes les propriétés du dossier à l’exception **PR_DISPLAY_NAME et** **PR_COMMENT**. 
    
- **Appelez CopyProps**, en passant **PR_DISPLAY_NAME** et **PR_COMMENT** dans le tableau Include. 
    
Dans ce cas, **CopyProps** est le meilleur choix, car il est destiné à être utilisé pour copier un petit ensemble de propriétés et est l’appel le plus simple à implémenter. 
  
Pour copier ou déplacer uniquement les propriétés du dossier, sans inclure de messages, appelez la méthode **IMAPIProp::CopyTo** du dossier et excluez les propriétés suivantes : 
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
Les méthodes de copie peuvent renvoyer S_OK, indiquant le nombre total de réussites, MAPI_W_PARTIAL_COMPLETION, indiquant une réussite partielle ou une erreur. Si MAPI_W_PARTIAL_COMPLETION est renvoyé, utilisez la macro **HR_FAILED** pour accéder à une erreur plus spécifique. Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
  
Si vous copiez des messages d’une banque de messages vers une autre et qu’Unicode n’est pas pris en charge par les deux, sachez que les informations peuvent être perdues en raison de la conversion de page de code. En règle générale, vous ne pouvez pas savoir si les magasins de messages prend en charge un format ou les deux, ce qui rend impossible de déterminer s’il faut copier les propriétés de texte en tant que chaînes ASCII ou en tant que chaînes Unicode. Si vous prise en charge Unicode, essayez d’effectuer une copie Unicode ; si elle échoue avec la valeur d’MAPI_E_BAD_CHARWIDTH, recourez à ASCII.
  

