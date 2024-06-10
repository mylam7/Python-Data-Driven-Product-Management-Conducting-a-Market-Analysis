# Python-Product-Management-Conducting-a-Market-Analysis

{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "316d2306",
   "metadata": {},
   "outputs": [],
   "source": [
    "#Help the fitness studio explore interest in workouts at a global and national level."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "id": "350e8e62",
   "metadata": {},
   "outputs": [],
   "source": [
    "import pandas as pd\n",
    "import matplotlib.pyplot as plt"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 39,
   "id": "727218e5",
   "metadata": {},
   "outputs": [],
   "source": [
    "df_workout_geo = pd.read_csv(\"C:\\\\Users\\\\My Lam\\\\downloads\\\\data\\\\workout_geo.csv\", index_col =0)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 17,
   "id": "b8ec9c4b",
   "metadata": {},
   "outputs": [],
   "source": [
    "df_workout = pd.read_csv(\"C:\\\\Users\\\\My Lam\\\\downloads\\\\data\\\\workout.csv\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 47,
   "id": "0d6e48b4",
   "metadata": {},
   "outputs": [],
   "source": [
    "df_three_keywords_geo = pd.read_csv(\"C:\\\\Users\\\\My Lam\\\\downloads\\\\data\\\\three_keywords_geo.csv\", index_col = 0)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "id": "853babdf",
   "metadata": {},
   "outputs": [],
   "source": [
    "df_three_keywords = pd.read_csv(\"C:\\\\Users\\\\My Lam\\\\downloads\\\\data\\\\three_keywords.csv\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 43,
   "id": "782b291d",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>workout_2018_2023</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>country</th>\n",
       "      <th></th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Guam</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Falkland Islands (Islas Malvinas)</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Cook Islands</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Brunei</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Palau</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Tokelau</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Tuvalu</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>U.S. Outlying Islands</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Vatican City</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Wallis &amp; Futuna</th>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>250 rows × 1 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "                                   workout_2018_2023\n",
       "country                                             \n",
       "Guam                                             NaN\n",
       "Falkland Islands (Islas Malvinas)                NaN\n",
       "Cook Islands                                     NaN\n",
       "Brunei                                           NaN\n",
       "Palau                                            NaN\n",
       "...                                              ...\n",
       "Tokelau                                          NaN\n",
       "Tuvalu                                           NaN\n",
       "U.S. Outlying Islands                            NaN\n",
       "Vatican City                                     NaN\n",
       "Wallis & Futuna                                  NaN\n",
       "\n",
       "[250 rows x 1 columns]"
      ]
     },
     "execution_count": 43,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df_workout_geo"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 21,
   "id": "b706e4be",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>month</th>\n",
       "      <th>workout_worldwide</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>2018-03</td>\n",
       "      <td>59</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>2018-04</td>\n",
       "      <td>61</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>2018-05</td>\n",
       "      <td>57</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>2018-06</td>\n",
       "      <td>56</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>2018-07</td>\n",
       "      <td>51</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>56</th>\n",
       "      <td>2022-11</td>\n",
       "      <td>47</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>57</th>\n",
       "      <td>2022-12</td>\n",
       "      <td>44</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>58</th>\n",
       "      <td>2023-01</td>\n",
       "      <td>62</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>59</th>\n",
       "      <td>2023-02</td>\n",
       "      <td>57</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>60</th>\n",
       "      <td>2023-03</td>\n",
       "      <td>55</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>61 rows × 2 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "      month  workout_worldwide\n",
       "0   2018-03                 59\n",
       "1   2018-04                 61\n",
       "2   2018-05                 57\n",
       "3   2018-06                 56\n",
       "4   2018-07                 51\n",
       "..      ...                ...\n",
       "56  2022-11                 47\n",
       "57  2022-12                 44\n",
       "58  2023-01                 62\n",
       "59  2023-02                 57\n",
       "60  2023-03                 55\n",
       "\n",
       "[61 rows x 2 columns]"
      ]
     },
     "execution_count": 21,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df_workout"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 48,
   "id": "560d52e4",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>home_workout_2018_2023</th>\n",
       "      <th>gym_workout_2018_2023</th>\n",
       "      <th>home_gym_2018_2023</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Country</th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Gibraltar</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Lesotho</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Guam</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Botswana</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Brunei</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Tokelau</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Tuvalu</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>U.S. Outlying Islands</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Vatican City</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Wallis &amp; Futuna</th>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>250 rows × 3 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "                       home_workout_2018_2023  gym_workout_2018_2023  \\\n",
       "Country                                                                \n",
       "Gibraltar                                 NaN                    NaN   \n",
       "Lesotho                                   NaN                    NaN   \n",
       "Guam                                      NaN                    NaN   \n",
       "Botswana                                  NaN                    NaN   \n",
       "Brunei                                    NaN                    NaN   \n",
       "...                                       ...                    ...   \n",
       "Tokelau                                   NaN                    NaN   \n",
       "Tuvalu                                    NaN                    NaN   \n",
       "U.S. Outlying Islands                     NaN                    NaN   \n",
       "Vatican City                              NaN                    NaN   \n",
       "Wallis & Futuna                           NaN                    NaN   \n",
       "\n",
       "                       home_gym_2018_2023  \n",
       "Country                                    \n",
       "Gibraltar                             NaN  \n",
       "Lesotho                               NaN  \n",
       "Guam                                  NaN  \n",
       "Botswana                              NaN  \n",
       "Brunei                                NaN  \n",
       "...                                   ...  \n",
       "Tokelau                               NaN  \n",
       "Tuvalu                                NaN  \n",
       "U.S. Outlying Islands                 NaN  \n",
       "Vatican City                          NaN  \n",
       "Wallis & Futuna                       NaN  \n",
       "\n",
       "[250 rows x 3 columns]"
      ]
     },
     "execution_count": 48,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df_three_keywords_geo"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 23,
   "id": "9c312495",
   "metadata": {
    "scrolled": true
   },
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>month</th>\n",
       "      <th>home_workout_worldwide</th>\n",
       "      <th>gym_workout_worldwide</th>\n",
       "      <th>home_gym_worldwide</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>2018-03</td>\n",
       "      <td>12</td>\n",
       "      <td>16</td>\n",
       "      <td>10</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>2018-04</td>\n",
       "      <td>12</td>\n",
       "      <td>18</td>\n",
       "      <td>10</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>2018-05</td>\n",
       "      <td>13</td>\n",
       "      <td>16</td>\n",
       "      <td>9</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>2018-06</td>\n",
       "      <td>12</td>\n",
       "      <td>17</td>\n",
       "      <td>9</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>2018-07</td>\n",
       "      <td>12</td>\n",
       "      <td>17</td>\n",
       "      <td>9</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>56</th>\n",
       "      <td>2022-11</td>\n",
       "      <td>11</td>\n",
       "      <td>18</td>\n",
       "      <td>12</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>57</th>\n",
       "      <td>2022-12</td>\n",
       "      <td>11</td>\n",
       "      <td>16</td>\n",
       "      <td>11</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>58</th>\n",
       "      <td>2023-01</td>\n",
       "      <td>17</td>\n",
       "      <td>22</td>\n",
       "      <td>15</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>59</th>\n",
       "      <td>2023-02</td>\n",
       "      <td>14</td>\n",
       "      <td>21</td>\n",
       "      <td>12</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>60</th>\n",
       "      <td>2023-03</td>\n",
       "      <td>13</td>\n",
       "      <td>19</td>\n",
       "      <td>12</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>61 rows × 4 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "      month  home_workout_worldwide  gym_workout_worldwide  home_gym_worldwide\n",
       "0   2018-03                      12                     16                  10\n",
       "1   2018-04                      12                     18                  10\n",
       "2   2018-05                      13                     16                   9\n",
       "3   2018-06                      12                     17                   9\n",
       "4   2018-07                      12                     17                   9\n",
       "..      ...                     ...                    ...                 ...\n",
       "56  2022-11                      11                     18                  12\n",
       "57  2022-12                      11                     16                  11\n",
       "58  2023-01                      17                     22                  15\n",
       "59  2023-02                      14                     21                  12\n",
       "60  2023-03                      13                     19                  12\n",
       "\n",
       "[61 rows x 4 columns]"
      ]
     },
     "execution_count": 23,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df_three_keywords"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 26,
   "id": "5a3d6c3b",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 1200x600 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "#When was the global search for 'workout' at its peak?\n",
    "plt.figure(figsize=(12,6))\n",
    "plt.plot(df_workout[\"month\"], df_workout[\"workout_worldwide\"])\n",
    "plt.xticks(rotation=90)\n",
    "plt.show()\n",
    "\n",
    "year_str = \"2020\"\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 42,
   "id": "f037d035",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "workout_2018_2023    100.0\n",
      "Name: United States, dtype: float64\n"
     ]
    }
   ],
   "source": [
    "#What country has the highest interest for workouts among the following: United States, Australia, or Japan\n",
    "print(df_workout_geo.loc[\"United States\"])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 44,
   "id": "1838458b",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "workout_2018_2023    77.0\n",
      "Name: Australia, dtype: float64\n"
     ]
    }
   ],
   "source": [
    "print(df_workout_geo.loc[\"Australia\"])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 45,
   "id": "7d54725c",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "workout_2018_2023    1.0\n",
      "Name: Japan, dtype: float64\n"
     ]
    }
   ],
   "source": [
    "print(df_workout_geo.loc[\"Japan\"])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 46,
   "id": "39ece1af",
   "metadata": {},
   "outputs": [],
   "source": [
    "top_country = \"United States\""
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 55,
   "id": "bfbdba67",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "home_workout_2018_2023    52.0\n",
      "gym_workout_2018_2023     38.0\n",
      "home_gym_2018_2023        10.0\n",
      "Name: Philippines, dtype: float64\n"
     ]
    }
   ],
   "source": [
    "#You'd be interested in expanding your virtual home workouts offering to either the Philippines or Malaysia. Which of the two countries has the highest interest in home workouts? Identify the country and save it as home_workout_geo.\n",
    "print(df_three_keywords_geo.loc[\"Philippines\", :])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 54,
   "id": "16b3d7c2",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "home_workout_2018_2023    47.0\n",
      "gym_workout_2018_2023     38.0\n",
      "home_gym_2018_2023        15.0\n",
      "Name: Malaysia, dtype: float64\n"
     ]
    }
   ],
   "source": [
    "print(df_three_keywords_geo.loc[\"Malaysia\", :])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 52,
   "id": "2e6cdd01",
   "metadata": {},
   "outputs": [],
   "source": [
    "home_workout_geo = \"Philippines\""
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.9.13"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
