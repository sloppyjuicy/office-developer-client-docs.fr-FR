---
title: Lecture et analyse d’une périodicité
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 75113097-b3ae-4d20-9796-85c62a592ef0
ms.openlocfilehash: 3d2dbfe54b525324ab9a016b83b706905eeaf7fb
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369669"
---
# <a name="read-and-parse-a-recurrence-pattern"></a>Lecture et analyse d’une périodicité
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI peut être utilisé pour lire et consulter une récurrence pour un rendez-vous.
  
Pour plus d’informations sur la façon de télécharger, d’afficher et d’exécuter le code à partir du projet d’application MFCMAPI référencé dans cette rubrique, voir [Installer les exemples utilisés dans cette section](how-to-install-the-samples-used-in-this-section.md).

### <a name="to-parse-a-recurrence-blob"></a>Pour parer un blob de récurrence

1. Ouvrez un élément de rendez-vous. Pour plus d’informations sur l’ouverture d’un message, voir [Opening a Message](opening-a-message.md).
    
2. Récupérez la propriété **nommée dispidApptRecur** (propriété canonique [PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)). Pour plus d’informations sur la récupération des propriétés nommées, voir [PROPRIÉTÉS nommées MAPI](mapi-named-properties.md).
    
3. Suivez les instructions de [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28EXCHG.80%29.aspx) pour lire la structure de la récurrence des rendez-vous. 
    
L’application  `BinToAppointmentRecurrencePatternStruct` de référence MFCMAPI illustre la dernière étape avec la fonction dans le fichier source InterpretProp2.cpp du projet MFCMapi. La  `BinToAppointmentRecurrencePatternStruct` fonction prend un pointeur vers une mémoire tampon en mémoire en tant que paramètre. L’application MFCMAPI obtient cette mémoire tampon en mappant d’abord la propriété nommée **dispidApptRecur** à une balise de propriété, puis en demandant la valeur de la propriété à l’aide de la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . Si la propriété est trop grande pour être récupérée à l’aide de la méthode **GetProps** , MFCMAPI ouvre une interface de flux pour récupérer la propriété à l’aide de la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) . L’application MFCMAPI lit ensuite les données hors du flux pour créer la mémoire tampon. 
  
Pour plus d’informations sur le format de la mémoire tampon, voir la propriété canonique [PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md). La majeure partie des données dans la mémoire tampon se compose de champs d’un nombre fixe d’octets, qui doivent être lus l’un après l’autre. Certains champs sont présents uniquement si d’autres champs contiennent certaines valeurs, et la taille de certains champs peut dépendre de la valeur d’autres champs. L’étude de la mémoire tampon pour lire les différents champs implique un grand nombre de comptabilité. MFCMAPI utilise une classe d’aide interne nommée  `CBinaryParser` pour encapsuler ce manuel. Par exemple, la  `CBinaryParser::GetDWORD` fonction vérifie si suffisamment d’octets restent dans la mémoire tampon pour lire un DWORD, puis lit la valeur et met à jour les pointeurs. 
  
Une fois la mémoire tampon en structure, l’application  `AppointmentRecurrencePatternStructToString` MFCMAPI utilise la fonction pour convertir la structure en chaîne à afficher à l’utilisateur. Ce n’est pas la même chaîne que Outlook afficherait, mais il s’agit à la place d’une vue brute des données sur lesquelles Outlook sa logique. 
  
Il est possible de rencontrer une mémoire tampon qui contient des données endommagées ou plus de données que nécessaire pour encoder une récurrence. Pour vous aider à identifier ces scénarios, l’application MFCMAPI assure le suivi de la quantité de données qui a été correctement analyse et de la quantité qui reste dans la mémoire tampon. Si les données restent dans la mémoire tampon une fois l’analyse terminée, MFCMAPI inclut ces « données indésirables » dans la structure afin qu’elles soient examinées.
  
Voici la liste complète de la  `BinToAppointmentRecurrencePatternStruct` fonction. 
  
```cpp
AppointmentRecurrencePatternStruct* BinToAppointmentRecurrencePatternStruct(ULONG cbBin, LPBYTE lpBin)
{
   if (!lpBin) return NULL;
   AppointmentRecurrencePatternStruct arpPattern = {0};
   CBinaryParser Parser(cbBin,lpBin);
   size_t cbBinRead = 0;
   arpPattern.RecurrencePattern = BinToRecurrencePatternStruct(cbBin,lpBin,&cbBinRead);
   Parser.Advance(cbBinRead);
   Parser.GetDWORD(&arpPattern.ReaderVersion2);
   Parser.GetDWORD(&arpPattern.WriterVersion2);
   Parser.GetDWORD(&arpPattern.StartTimeOffset);
   Parser.GetDWORD(&arpPattern.EndTimeOffset);
   Parser.GetWORD(&arpPattern.ExceptionCount);
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions)
   {
      arpPattern.ExceptionInfo = new ExceptionInfoStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExceptionInfo)
      {
         memset(arpPattern.ExceptionInfo,0,sizeof(ExceptionInfoStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].StartDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].EndDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].OriginalStartDate);
            Parser.GetWORD(&arpPattern.ExceptionInfo[i].OverrideFlags);
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength2);
               if (arpPattern.ExceptionInfo[i].SubjectLength2 && arpPattern.ExceptionInfo[i].SubjectLength2 + 1 
                  == arpPattern.ExceptionInfo[i].SubjectLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].SubjectLength2,&arpPattern.ExceptionInfo[i].Subject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_MEETINGTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].MeetingType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDERDELTA)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderDelta);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDER)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderSet);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength2);
               if (arpPattern.ExceptionInfo[i].LocationLength2 && arpPattern.ExceptionInfo[i].LocationLength2 
                  + 1 == arpPattern.ExceptionInfo[i].LocationLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].LocationLength2,&arpPattern.ExceptionInfo[i].Location);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_BUSYSTATUS)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].BusyStatus);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_ATTACHMENT)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].Attachment);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].SubType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_APPTCOLOR)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].AppointmentColor);
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock1Size);
   if (arpPattern.ReservedBlock1Size && arpPattern.ReservedBlock1Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock1Size,&arpPattern.ReservedBlock1);
   }
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions &&
      arpPattern.ExceptionInfo)
   {
      arpPattern.ExtendedException = new ExtendedExceptionStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExtendedException)
      {
         memset(arpPattern.ExtendedException,0,sizeof(ExtendedExceptionStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            if (arpPattern.WriterVersion2 >= 0x0003009)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightValue);
               if (arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize > sizeof(DWORD))
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize 
                     - sizeof(DWORD),&arpPattern.ExtendedException[i].ChangeHighlight.Reserved);
               }
            }
            Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE1Size);
            if (arpPattern.ExtendedException[i].ReservedBlockEE1Size &&
                arpPattern.ExtendedException[i].ReservedBlockEE1Size < _MaxReservedBlock)
            {
               Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE1Size,&arpPattern.ExtendedException[i].ReservedBlockEE1);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].StartDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].EndDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].OriginalStartDate);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharSubjectLength);
               if (arpPattern.ExtendedException[i].WideCharSubjectLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharSubjectLength,&arpPattern.ExtendedException[i].WideCharSubject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharLocationLength);
               if (arpPattern.ExtendedException[i].WideCharLocationLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharLocationLength,&arpPattern.ExtendedException[i].WideCharLocation);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE2Size);
               if (arpPattern.ExtendedException[i].ReservedBlockEE2Size && arpPattern.ExtendedException[i].ReservedBlockEE2Size < _MaxReservedBlock)
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE2Size,&arpPattern.ExtendedException[i].ReservedBlockEE2);
               }
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock2Size);
   if (arpPattern.ReservedBlock2Size && arpPattern.ReservedBlock2Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock2Size,&arpPattern.ReservedBlock2);
   }
   // Junk data remains.
   if (Parser.RemainingBytes() > 0)
   {
      arpPattern.JunkDataSize = Parser.RemainingBytes();
      Parser.GetBYTES(arpPattern.JunkDataSize,&arpPattern.JunkData);
   }
   AppointmentRecurrencePatternStruct* parpPattern = new AppointmentRecurrencePatternStruct;
   if (parpPattern)
   {
      *parpPattern = arpPattern;
   }
   return parpPattern;
}

```

## <a name="see-also"></a>Voir aussi

- [Utilisation de MAPI pour créer des Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

