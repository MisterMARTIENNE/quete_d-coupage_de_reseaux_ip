#quete découpage de reseaux ip

##découpage sysmétrique

On prend le pôle qui à le plus de besoin en équipement soit 50 IP on ajout les deux adresses reseaux et Broadcast on obtient 52 donc il nous faut 6 bits pour un total de 64 ip par branche de sous-réseaux.

|---| IP RESEAU | IP BROADCAST| IP de début de plage | IP de fin de plage |
| Pôle Informatique | 172.16.1.0/26 | 172.16.1.63 | 172.16.1.1 | 172.16.1.62 |
| Pôle développement | 172.16.1.64/26 | 172.16.1.127 | 172.16.1.65 | 172.16.1.126 |
| Pôle administratif | 172.16.1.128/26 | 172.16.1.191 | 172.16.1.129 | 172.16.1.190 |
| Pôle technicien | 172.16.1.192/26 | 172.16.1.255 | 172.16.1.193 | 172.16.1.254 |

##découpage asysmetrique

On prend d'avoir celui qui à le plus grand besoin soit 50 IP on ajout les deux adresses reseaux et broadcast on obtient 52 donc il nous faut 6 bits pour un total de 64 ip pour le pôle informatique.
On prend le deuxième en nombre de besoin soit 20 IP on ajout les deux adresses reseaux et broadcast on obtient 22 donc il nous faut 5 bits pour un total de 32 ip pour le pôle administratif.
On prend le troisième en nombre de besoin soit 15 IP on ajout les deux adresses reseaux et broadcast on obtient 17 donc il nous faut 5 bits pour un total de 32 ip pour le pôle technicien.
on prend le dernier en nombre soit 12 ip on ajout les deux reseaux et broadcast on obtient 14 donc il nous faut 4 bits pour un total de 16 ip pour le pôle développement.

|---| IP RESEAU | IP BRODCAST | Ip de début de plage | IP de fin de plage |
| Pôle informatique | 172.16.1.0/26 | 172.16.1.63 | 172.16.1.1 | 172.16.1.62 |
| Pôle administratif | 172.16.1.64/27 | 172.16.1.95 | 172.16.1.65 | 172.16.1.94 |
| Pôle technicien | 172.16.1.96/27 | 172.16.1.127 | 172.16.1.97 | 172.16.1.126 |
| Pôle dévellopement | 172.16.1.128/28 | 172.16.1.143 | 172.16.1.129 | 172.16.1.142 |
